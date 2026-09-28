# LK Study Studio: Electrical Circuit & Network

This is the production-ready React application for the LK Study Studio, seamlessly transforming your GitHub repository (`lalankumar99/Electrical-Circuits`) into a beautiful, mobile-first educational platform.

## Architecture & Single-File Implementation
To satisfy the single-file architectural constraint while providing standard Next.js/React capabilities, the entire application frontend, API integration, routing, and Markdown rendering logic are encapsulated within `App.tsx`. 

*   **Dynamic Synchronization:** It queries the GitHub REST API (`/git/trees/main?recursive=1`) on load to build the folder tree, meaning you **never need to redeploy or touch the code** when adding or changing Markdown files.
*   **Markdown Ecosystem:** Uses `react-markdown`, `remark-gfm` (for tables/strikethroughs), `remark-math` & `rehype-katex` (for LaTeX math rendering), and `isomorphic-dompurify` to ensure safe HTML/SVG execution.
*   **Routing:** Implements a lightweight internal view-state router to guarantee perfect functionality without requiring complex server-side file structures.

## Installation / Vercel Deployment (Next.js App Router)

1.  **Initialize Next.js:** 
    ```bash
    npx create-next-app@latest lk-study-studio --typescript --tailwind
    ```
2.  **Install Dependencies:**
    ```bash
    npm install lucide-react react-markdown remark-gfm remark-math rehype-katex isomorphic-dompurify
    ```
3.  **Include KaTeX CSS:** Add this to your main `layout.tsx` `<head>` or import it in your global CSS:
    ```html
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/katex.min.css" />
    ```
4.  **Replace Main File:** Copy the contents of the generated `App.tsx` and paste them directly into your `app/page.tsx` file (replacing the default Next.js landing page). The `"use client";` directive at the top ensures the React hooks function perfectly.
5.  **Deploy:** Push to a new GitHub repository and connect it to Vercel. 

## Content Management (How to update content)

You will manage all content directly inside the `lalankumar99/Electrical-Circuits` repository on GitHub. The website will automatically reflect changes.

### 1. Adding a New Subject/Folder
Simply create a new folder in your GitHub repository (e.g., `Advanced AC Circuits`). Drop Markdown (`.md`) files inside. The platform will automatically discover the folder and generate an interactive card for it on the Homepage.

### 2. Adding a Markdown File (Topic)
Create a `.md` file inside any folder. 
*   **Naming:** `Ohm-Law.md` will automatically display elegantly as "Ohm Law".
*   **Content:** Write standard Markdown. 

### 3. Adding Educational Callouts
To create beautiful, styled callouts, use standard blockquotes and start the text with specific keywords:

```markdown
> **Definition:** Voltage is the difference in electric potential between two points.

> **Important:** Always disconnect power before modifying the circuit.

> **Formula:** V = I * R

> **Example:** If I = 2A and R = 5Ω, then V = 10V.
```

### 4. Adding Mathematical Equations
Use standard LaTeX syntax:
*   Inline: `$V = I \times R$`
*   Block: 
    ```math
    $$ I = \frac{V}{R} $$
    ```

### 5. Adding Images
Upload your image to the GitHub repository (e.g., inside an `images` folder or next to the Markdown file). Reference it relatively:
```markdown
![Circuit Diagram](./images/circuit-1.png)
```
The App automatically resolves the relative path to the correct raw GitHub URL.

### 6. Adding a Practical Experiment
Create a folder named exactly `Practical` anywhere in your repository (or in the root). Any `.md` files placed inside this folder will automatically be aggregated and featured in the **Practical Lab** section of the website.

### 7. Cache Revalidation & Webhooks
Currently, the app fetches the live tree from GitHub on every initial client load, ensuring users always see the latest files. Because GitHub's raw content CDN is heavily cached, newly committed files may take up to 5 minutes to reflect perfectly. For enterprise-grade instant updates in the future, you can configure Next.js server-side Incremental Static Regeneration (ISR) and trigger it via GitHub Webhooks, though the current client-side dynamic fetch ensures zero-maintenance synchronization out of the box.