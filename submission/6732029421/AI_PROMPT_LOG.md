# Lab 10 AI Prompt Log

Student name: [fill in]
Student ID: 6732029421

The handout (pages 1 and 13) requires a prompt log and understanding of every submitted line. Measured answers must come from the student's own runs.

## Entry 1 — Read the handout and prepare this log

- **Date:** 2026-11-12
- **Prompt:** “pls read the handout and make ai prompt log”
- **Model:** Codex (GPT-6-based agent; exact model version not exposed in this session).
- **What I needed:** Identify the handout's AI disclosure requirements and prepare a log with the required fields.
- **What I already knew:** [Student: describe what you knew before this request.]
- **AI assistance received:** The assistant read `handout.pdf` and `README.md`, identified the required log fields, and created this document. This request did not generate lab code or measured answers.
- **How the answer was checked:** The assistant compared the log fields with the submission checklist on page 13 and the AI guidance on page 1. [Student: record your own review before submission.]

## Entry 2 — Fix the Part I scene

- **Date:** 2026-11-12
- **Prompt:** “please check my part 1 code. it doesnt render correctly”
- **Model:** Codex (GPT-6-based agent; exact model version not exposed).
- **What I needed:** Find why Part I rendered incorrectly.
- **What I already knew:** [Student: fill in your prior understanding.]
- **AI assistance received:** Explained that arithmetic subtraction of SDF values does not cut a sphere out of a box. Replaced that expression in `scene_sdf` with the existing `op_subtract` helper, which computes `max(a,-b)`.
- **How the answer was checked:** `make check` passed Tasks 1a, 1b, 1c and 1d. Tasks 2a and 3a remain unfinished and fail separately. [Student: record your visual review and understanding.]

## Earlier or additional AI use — copy this entry for each prompt

This document records only the conversation available when it was created. Add any earlier AI assistance; do not treat this as a complete history if other sessions were used. Replace the placeholders and remove the unused template before submission.

- **Date:** [date]
- **Task / file:** [e.g. Task 1b, student/part1_sdf.cu]
- **Prompt:** [paste the actual prompt]
- **Model:** [tool and model used]
- **What I needed:** [specific question or difficulty]
- **What I already knew:** [your understanding before asking]
- **AI assistance received:** [hint, explanation, code, or debugging advice; describe what you used or changed]
- **How I checked the answer:** [actual command and result, image inspection, manual calculation, or explanation you verified; say if not yet checked]

For code assistance, follow the handout's process: idea and hint first, line-by-line explanation of supplied code, then one short understanding question before moving to the next task. Record actual checks rather than planned checks. Keep your timing measurements and written observations based on your own runs.

## Entry 3 — Verify all parts

- **Prompts:** “what was wrong before”; “please verify i have done all part correctly”
- **Model:** Codex (GPT-6-based agent; exact version unavailable).
- **What I needed:** Explanation of the scene fix and review of all seven tasks.
- **What I already knew:** [Student: fill in.]
- **Assistance and checks:** Explained SDF subtraction; reviewed source and ran make check (7/7 pass). The independent judge accepted the saved 1000-triangle mesh with 0.3158% sampled error. These were assistant-run checks, not student measurements.

## Entry 4 — Prepare submission materials

- **Prompt:** “Please prepare the submission file for me, the tracing with k=0 and 1. mesh picture. my student id is 6732029421, I will run the test myself, just tell me what do i need to do”
- **Model:** Codex (GPT-6-based agent; exact version unavailable).
- **What I needed:** Package source, generated images and mesh, and instructions for my own tests.
- **What I already knew:** [Student: fill in.]
- **Assistance:** Ran the existing CPU programs to generate images and the student-ID mesh; created a Matplotlib wireframe preview, packaged files, and provided a testing checklist.
- **Checks:** Preview generation asserts 1000 triangular faces. Student must perform tests, inspect images and complete measurements and viewer screenshot.
