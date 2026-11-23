---
name: ai-workflow-evaluation
description: Design an evaluation plan for an AI workflow using synthetic examples, explicit scoring, and release criteria.
---

# Evaluate an AI workflow

1. Identify one user task, who performs it, and what a usable result looks like. State whether the workflow drafts, recommends, or takes an action.
2. Choose a baseline such as the current manual workflow, a rules-based process, or the previous model. Use the same inputs for each.
3. Create synthetic cases for ordinary inputs, missing fields, contradictory instructions, and cases that should go to a human. Record expected behavior before running them.
4. Score correctness, evidence, and action safety separately. Award one point per criterion met. Flag any unapproved external action or disclosure as a critical failure.
5. Choose a release threshold before scoring. Report case counts and failure categories. Keep part of the case set for regression checks after changes.

## Example

For a CRM follow-up drafting tool, provide a fictional account with a missing renewal date. A passing draft uses confirmed details, flags the missing date, and leaves the message for human review. An invented date fails correctness. Sending the draft without approval is a critical failure.
