# Linear and Non-linear Electrical Circuits

## 1. Linear Circuit

A **linear circuit** is a circuit in which the relationship between voltage and current is proportional.

\[
V \propto I
\]

For a constant resistance:

\[
V = IR
\]

### Linear V-I Characteristic

<svg xmlns="http://www.w3.org/2000/svg" width="720" height="430" viewBox="0 0 720 430">
  <rect width="720" height="430" fill="#ffffff"/>
  <text x="360" y="35" text-anchor="middle"
        font-family="Arial" font-size="24" font-weight="700">
    Linear V-I Characteristic
  </text>

  <line x1="100" y1="360" x2="650" y2="360"
        stroke="#111827" stroke-width="3"/>
  <polygon points="650,360 636,353 636,367" fill="#111827"/>

  <line x1="100" y1="360" x2="100" y2="70"
        stroke="#111827" stroke-width="3"/>
  <polygon points="100,70 93,84 107,84" fill="#111827"/>

  <line x1="100" y1="360" x2="600" y2="95"
        stroke="#2563eb" stroke-width="5"/>

  <text x="665" y="368" font-family="Arial" font-size="18">I</text>
  <text x="85" y="60" font-family="Arial" font-size="18">V</text>

  <text x="615" y="88"
        font-family="Arial" font-size="18"
        fill="#2563eb">
    Straight Line
  </text>

  <text x="360" y="405"
        text-anchor="middle"
        font-family="Arial" font-size="17">
    Current (I)
  </text>

  <text x="35" y="215"
        transform="rotate(-90 35 215)"
        text-anchor="middle"
        font-family="Arial" font-size="17">
    Voltage (V)
  </text>
</svg>

---

## 2. Characteristics of Linear Circuit

- Voltage and current relationship is proportional.
- The V-I characteristic is a straight line.
- Circuit parameters are considered constant for the operating condition.
- For a constant resistor:

\[
V = IR
\]

### Example

Given:

\[
R = 10\Omega
\]

For:

\[
V = 10V
\]

\[
I = \frac{V}{R}
\]

\[
I = \frac{10}{10}=1A
\]

If voltage becomes `20 V`:

\[
I = \frac{20}{10}=2A
\]

Therefore, voltage doubled and current also doubled.

---

# 3. Non-linear Circuit

A **non-linear circuit** is a circuit in which the relationship between voltage and current is not proportional.

\[
V \not\propto I
\]

The V-I characteristic is generally a curved line instead of a straight line.

### Non-linear V-I Characteristic

<svg xmlns="http://www.w3.org/2000/svg" width="720" height="430" viewBox="0 0 720 430">
  <rect width="720" height="430" fill="#ffffff"/>

  <text x="360" y="35"
        text-anchor="middle"
        font-family="Arial"
        font-size="24"
        font-weight="700">
    Non-linear V-I Characteristic
  </text>

  <line x1="100" y1="360" x2="650" y2="360"
        stroke="#111827" stroke-width="3"/>
  <polygon points="650,360 636,353 636,367" fill="#111827"/>

  <line x1="100" y1="360" x2="100" y2="70"
        stroke="#111827" stroke-width="3"/>
  <polygon points="100,70 93,84 107,84" fill="#111827"/>

  <path d="M100 360
           C180 358, 235 350, 290 325
           C355 296, 405 245, 455 190
           C505 135, 555 103, 620 88"
        fill="none"
        stroke="#dc2626"
        stroke-width="5"/>

  <text x="625" y="78"
        font-family="Arial"
        font-size="18"
        fill="#dc2626">
    Curved Line
  </text>

  <text x="665" y="368"
        font-family="Arial"
        font-size="18">
    I
  </text>

  <text x="85" y="60"
        font-family="Arial"
        font-size="18">
    V
  </text>

  <text x="360" y="405"
        text-anchor="middle"
        font-family="Arial"
        font-size="17">
    Current (I)
  </text>

  <text x="35" y="215"
        transform="rotate(-90 35 215)"
        text-anchor="middle"
        font-family="Arial"
        font-size="17">
    Voltage (V)
  </text>
</svg>

---

## 4. Characteristics of Non-linear Circuit

- Voltage and current relationship is not proportional.
- V-I characteristic is generally curved.
- Circuit behavior changes with operating point.
- A single constant resistance does not describe the complete V-I characteristic.

### Example

A **diode** is an example of a non-linear electrical element because its current does not increase proportionally with voltage over its complete operating characteristic.

---

# 5. Difference Between Linear and Non-linear

| Linear | Non-linear |
|---|---|
| V-I relationship is proportional | V-I relationship is not proportional |
| Characteristic is a straight line | Characteristic is generally curved |
| Response is proportional to input | Response is not directly proportional to input |
| Constant parameters for the operating condition | Parameters/behavior can vary with operating point |
| Example: constant resistor | Example: diode |

---

# 6. Quick Revision

> **Linear → Proportional relationship → Straight-line characteristic**

> **Non-linear → Non-proportional relationship → Curved characteristic**

### Important Formula

\[
V = IR
\]

Where:

- `V` = Voltage
- `I` = Current
- `R` = Resistance

---

## Exam Definitions

### Linear Circuit

A circuit in which the voltage-current relationship is proportional for the specified operating condition is called a **linear circuit**.

### Non-linear Circuit

A circuit in which the voltage-current relationship is not proportional is called a **non-linear circuit**.