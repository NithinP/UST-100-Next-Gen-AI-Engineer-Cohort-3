# Assignment 3 — Prompt Engineering on Real-World Scenarios

Written prompt-engineering assignment: 13 real-world scenarios (ambiguous context, adversarial inputs, multi-step reasoning, few-shot vs zero-shot judgment, output/format control, meta-prompting/self-critique, failure recovery, and a full prompting strategy design).

## Files

- `Prompt_Engineering_Assignment3.md` — the full written assignment (renders directly on GitHub with formatting).
- `UST_Assignment3_Prompt_Engineering_Report.pdf` — the same content as a formatted PDF report.

Note: this assignment is a written/design exercise (no dataset, code, or notebook required per the assignment brief).

## Structure

For each of the 13 questions: a full usable prompt, an explanation of the structural design choices, the prompting technique used (zero-shot / few-shot / Chain-of-Thought / Tree-of-Thought / hybrid) and why, the failure modes it prevents, and at least one alternative prompt design.

## Key takeaways

- **Extraction stages should suppress reasoning and lock to a strict schema** (with an explicit "UNKNOWN" fallback) to minimize hallucination risk at the earliest point in a pipeline.
- **Reasoning stages should enforce structured Chain-of-Thought** for novel/ambiguous/high-stakes tasks, and few-shot examples for recurring, stable-structure tasks (e.g. classification).
- **Validation should be a separate pass/call**, not the same context that generated the answer — mirrors both prompt-injection defense (Q3) and self-critique loop-breaking (Q10).
- **Every self-correction or retry loop needs a hard stop** to avoid unbounded iteration.
- **Format constraints (word limits, banned hedge phrases, required tables) control verbosity more reliably than vague instructions** like "be concise."
