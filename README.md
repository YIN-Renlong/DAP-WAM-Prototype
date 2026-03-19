# A Dynamic Assessment Protocol (DAP) Prototype

This repository contains a functional prototype of the **Dynamic Assessment Protocol (DAP)** and its core instrument, the **Weighted Authorship Matrix (WAM)**. It was created as a tangible deliverable for the Master's Thesis proposal titled: *A Dynamic Protocol (DAP) Design for Signal Clarity in Generative AI Education: An HCI-Ethical Approach*.

## View the Live Prototype

The prototype is a self-contained HTML file deployed using GitHub Pages. You can view and interact with the live WAM builder here:

[https://YIN-Renlong.github.io/DAP-WAM-Prototype/dap-prototype.html](https://YIN-Renlong.github.io/DAP-WAM-Prototype/dap-prototype.html)

---

## System Design & Logic Engine

The power of the DAP is not the table itself, but the **interconnected logic** that governs it. The prototype implements this logic as a **Constrained User Interface**, which prevents instructors from creating pedagogically flawed or procedurally unjust assessment schemes.

### 1. The Interconnected Logic (The "Why")

The matrix columns are not independent variables; they form a coupled system designed to maintain equilibrium between student agency, academic integrity, and fair assessment. The logic engine actively enforces this by preventing "Anti-Patterns":

#### 🟥 Anti-Pattern 1: The Free-Rider Loophole
- **Condition:** High `Assessment Weight` + High AI Allowance (`Tooling`) + Low `Evidence Strength`.
- **Risk:** Creates a loophole for unverified, AI-generated work to receive significant credit, collapsing academic integrity.
- **DAP Solution:** The logic engine detects this combination (`Weight >= 25%`, `AI Allowed`, `Evidence <= E1`) and flags it as a **"Security Risk,"** disabling the ability to publish the matrix until the evidence requirement is strengthened.

#### 🟨 Anti-Pattern 2: The Surveillance Trap
- **Condition:** Low `Assessment Weight` + High `Evidence Strength`.
- **Risk:** Creates excessive, unnecessary "False Difficulty" (Wang, 2026) by forcing students to provide strong proof for a component the instructor has deemed low-value. This is a poor user experience (HCI failure).
- **DAP Solution:** The logic engine flags this (`Weight <= 10%`, `Evidence >= E3`) as an **"HCI Warning"** and recommends a lower evidence requirement, reducing friction.

This logic ensures that assessment is always aligned with the stated learning objectives, moving the pedagogical focus from "Process Certainty" (manual labor) to "Outcome Certainty" (verifiable mastery).

### 2. Technical Architecture (The "How")

This prototype is a self-contained, client-side web application built with a minimalist stack to ensure portability and ease of use.

- **Framework:** **React.js** (via CDN) is used for state management and creating a reactive user interface.
- **Styling:** **Tailwind CSS** (via CDN) is used for rapid, utility-first styling.
- **The Logic Engine:** A core JavaScript function (`getRowErrors`) takes the state of a matrix row as input, applies the interconnected rules described above, and returns an array of error messages.
- **State Management:** The entire WAM is held in a single state variable (`useState`). Any change to an input field triggers a re-render, which re-runs the logic engine and instantly updates the UI with any warnings.

The entire application runs in the browser with **no build step or server required**, making it a perfect demonstration of the DAP's core principles in a shareable format.

### Thesis Context
- **Author:** YIN Renlong
- **Supervisor:** Prof. Katherine Verbert
- **Thesis Mentor:** John Kelly Tamargo
