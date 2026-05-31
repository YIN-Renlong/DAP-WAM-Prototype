- # Dynamic Assessment Protocol (DAP): System Architecture & Prototype

  This repository contains the functional prototype of the **Weighted Authorship Matrix (WAM)**, the core instrument of the **Dynamic Assessment Protocol (DAP)**. It is a tangible deliverable for the Master's Thesis: *A Dynamic Protocol (DAP) Design for Signal Clarity in Generative AI Education: An HCI-Ethical Approach*.

  ## 🔗 View the Live Prototype
  **[Access the Interactive WAM Builder Here](https://YIN-Renlong.github.io/DAP-WAM-Prototype/dap-prototype.html)**

  ---

  ## Part 1: Theoretical Architecture & The Re-definition of "Evidence"

  In traditional, pre-AI pedagogy, submitting a static file (e.g., 500 lines of manual code) was considered **"Strong Evidence"** of learning. The *process* of manual typing guaranteed the student's cognitive engagement (Process Certainty). 

  In the GenAI era, static files are computationally commoditized. Therefore, the DAP fundamentally redefines "Evidence." Evidence no longer measures *how hard a student worked*; it measures *how difficult it is for a student to fake their understanding using AI* (Outcome Certainty).

  *   **E1 (Weak Evidence):** Static artifacts (code files, essays, basic execution logs). Highly vulnerable to undetected AI generation. A student can produce E1 in seconds with zero comprehension.
  *   **E2 (Moderate Evidence):** Process artifacts (Git commit histories, documented debugging logs, unit tests). Proves the student engaged with the logic, though AI may have assisted.
  *   **E3 (Strong Evidence):** Cognitive artifacts (Architectural Diagrams, Design Rationales). The student must explain *why* a system is built a certain way. AI can write code, but defending the architecture requires a "System Auditor" mindset.
  *   **E4 (Live Contextual):** The ultimate unfakeable proof. A 10-minute live viva/interrogation where the student must verbally defend specific logic choices to the assessor.

  ---

  ## Part 2: The "Tier 1 Paradox" & Procedural Justice

  The DAP explicitly maps out the logical trap of banning AI (**Tier 1: Foundational**). 

  If an instructor strictly forbids AI, they face a paradox: **How do they prove the student didn't use it?** 
  There are only two methods:
  1.  **Unethical Surveillance:** Forcing students to install invasive screen-recording or keystroke-tracking software. The DAP's Value-Sensitive Design explicitly rejects this due to privacy, equity, and anxiety concerns.
  2.  **The Honor System (E1):** The student submits the finished code, and the instructor simply has to trust them. 

  **The General Case of Systemic Failure:**
  What happens if a student submits E1 (Weak Evidence) under a Tier 1 (No AI) policy, and the professor says, *"I don't trust you; this looks like AI"*? 

  Without the DAP, this results in **Epistemic Injustice**. The student is accused based on "vibes" or flawed AI detectors, and has no way to prove a negative (that they *didn't* use a tool).

  **The DAP Solution (Procedural Justice):**
  If a professor utilizes the WAM, they enter a digital contract. If they suspect cheating, they cannot arbitrarily fail the student based on suspicion of E1 evidence. The DAP forces them to trigger **Layer 3: Contextual Verification**. They must schedule a live viva (E4) and ask: *"Explain lines 10-20."* If the student can explain the logic, they pass. The DAP replaces a culture of "policing and suspicion" with one of "verifiable outcome certainty."

  ---

  ## Part 3: The Universal System Logic (General Case)

  The WAM is an interactive "Boundary Object" (Star & Griesemer, 1989). Its drop-down menus are not independent choices; they are mathematically and pedagogically coupled variables. The UI acts as a logic engine to enforce **Constructive Alignment**.

  The universal logic of the DAP is defined by three interconnected ratios:

  1.  **The Verification Equilibrium ($Tooling \propto Evidence$):** As the computational agency of the AI increases (from "Student Only" to "AI Allowed"), the cognitive burden on the student must shift from *generation* to *verification*. High AI allowance demands higher Evidence Strength.
  2.  **The Scrutiny Resolution ($Component \propto Granularity$):** The "Zoom Level" of disclosure must match the abstraction level of the task. If a student is designing "System Architecture" (Macro), forcing "Line-Level" (Micro) disclosure is an HCI failure that creates cognitive overload.
  3.  **The Mastery Lock ($Component \propto Weight$):** The grading weight must reflect the specific Persona being tested. In a Tier 3 (Architectural) class, manual typing should carry low weight, while system verification carries high weight.

  ---

  ## Part 4: The Constraint Engine (Encoded Rules)

  To prevent instructors from building flawed rubrics, the React prototype actively scans the WAM state for specific "Anti-Patterns" and throws UI warnings/errors.

  #### 🟥 Anti-Pattern 1: The Free-Rider Loophole
  *   **Condition:** `(Weight >= 25%)` AND `(Tooling == 'AI Allowed' OR 'Hybrid')` AND `(Evidence <= E1)`
  *   **System Response:** `TRIGGER ERROR` (Disables publishing)
  *   **Architectural Rationale:** This prevents the total collapse of assessment integrity. If a task is worth a massive portion of the grade, and AI is allowed to do the heavy lifting, the instructor *must* demand moderate-to-strong cognitive evidence (E2/E3) that the student can audit the AI's output. Accepting Weak Evidence (E1) here creates a massive Epistemic Blind Spot where students get "A"s for clicking "Generate."

  #### 🟨 Anti-Pattern 2: The Surveillance Trap (HCI Friction)
  *   **Condition:** `(Weight <= 10%)` AND `(Evidence >= E3)`
  *   **System Response:** `TRIGGER WARNING`
  *   **Architectural Rationale:** Enforces the HCI principle of minimizing user friction. Demanding rigorous cognitive proof (e.g., a multi-page rationale or live viva) for a trivial, low-stakes task (e.g., adding code comments) creates disproportionate cognitive overload ("False Difficulty"). 

  #### 🟨 Anti-Pattern 3: Manual Labor Misalignment
  *   **Condition:** `(Component == 'Syntax/Boilerplate')` AND `(Weight > 20%)` AND `(Tooling == 'AI Allowed')`
  *   **System Response:** `TRIGGER WARNING`
  *   **Architectural Rationale:** Prevents grading the AI instead of the student. If a course heavily weights the manual production of syntax, the instructor must restrict tooling to "Student Only." If they allow AI to type the syntax, that component's weight must be reduced, shifting the grading weight to architectural design or debugging.

  #### 🟨 Anti-Pattern 4: Granularity Mismatch (Conceptual Design Rule)
  *   **Condition:** `(Component == 'Macro/Architecture')` AND `(Granularity == 'Line-Level')`
  *   **Architectural Rationale:** Prevents the "Transparency Paradox." Forcing students to document microscopic AI usage (e.g., "AI autocompleted line 42") on macroscopic tasks destroys their workflow and incentivizes them to hide their AI use entirely to avoid the administrative burden.

  ---
  **Thesis Context**
  - **Author:** YIN Renlong
  - **Supervisor:** Prof. Katherine Verbert
  - **Thesis Mentor:** John Kelly Tamargo
