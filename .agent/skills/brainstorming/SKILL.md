---
name: brainstorming
description: Facilitates the exploration of ideas and requirements before implementation. Use when the user wants to discuss a new feature, a vague idea, or needs to clarify requirements before coding.
---

# Brainstorming Ideas Into Designs

## When to use this skill
- Before starting any creative work (creating features, building components).
- When the user has a vague idea that needs refinement.
- When requirements are not fully defined.
- To explore user intent and design options before implementation.

## Workflow
1.  **Understand the Idea**: Query the user to clarify purpose and constraints.
2.  **Explore Approaches**: Propose multiple options with trade-offs.
3.  **Present Design**: Draft the design in small sections for validation.
4.  **Finalize & Document**: Create a design document and prepare for implementation.

## Instructions

### 1. Understanding the Idea
*   **Check Context**: Review existing project files, docs, and recent commits first.
*   **Ask Questions**:
    *   Ask **one question at a time**. Do not overwhelm the user.
    *   Prefer multiple-choice questions to reduce cognitive load.
    *   Focus on understanding purpose, constraints, and success criteria.

### 2. Exploring Approaches
*   Propose **2-3 different approaches**.
*   Highlight trade-offs for each option.
*   Lead with your recommended option and explain why.

### 3. Presenting the Design
*   Break the design into small sections (200-300 words).
*   **Incremental Validation**: Ask "Does this look right so far?" after each section.
*   Cover: Architecture, components, data flow, error handling, and testing.

### 4. After the Design
*   **Documentation**: Write the validated design to `docs/plans/YYYY-MM-DD-<topic>-design.md`.
*   **Commit**: Save the design document to git.
*   **Transition**: Ask "Ready to set up for implementation?" and if yes, use the `planning` skill.

## Principles
*   **YAGNI**: Ruthlessly remove unnecessary features.
*   **One Question Rule**: Never ask multiple questions in one turn.
*   **Flexibility**: Be ready to backtrack if the user corrects a misunderstanding.
