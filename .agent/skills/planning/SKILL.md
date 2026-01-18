---
name: planning
description: Generates comprehensive implementation plans from specs or requirements. Use when the user has a clear design or requirement and needs a step-by-step plan for execution.
---

# Creating Implementation Plans

## When to use this skill
- When you have a validated design or clear requirements.
- Before writing any code for a multi-step task.
- When the user asks for an implementation plan.

## Workflow
1.  **Context**: Ensure you have a clear understanding of the codebase and the task.
2.  **Granularity**: Break the work into bite-sized tasks (2-5 minutes each).
3.  **Drafting**: Write the plan following the required header and task structure.
4.  **Review**: Present the plan to the user for approval.
5.  **Save**: Write the plan to `docs/plans/YYYY-MM-DD-<feature-name>.md`.

## Instructions

### 1. Bite-Sized Granularity
Each step must be a single, verifiable action:
*   "Write the failing test"
*   "Run it to make sure it fails"
*   "Implement the minimal code"
*   "Run the tests to make sure they pass"
*   "Commit"

### 2. Plan Document Header
Every plan **MUST** start with this header:

```markdown
# [Feature Name] Implementation Plan

> **Note:** Execute this plan task-by-task.

**Goal:** [One sentence describing what this builds]

**Architecture:** [2-3 sentences about approach]

**Tech Stack:** [Key technologies/libraries]

---
```

### 3. Task Structure
Follow this structure for every task in the plan:

```markdown
### Task N: [Component/Feature Name]

**Files:**
- Create: `exact/path/to/file.py`
- Modify: `exact/path/to/existing.py:123-145`
- Test: `tests/exact/path/to/test.py`

**Step 1: Write the failing test**

```python
def test_specific_behavior():
    result = function(input)
    assert result == expected
```

**Step 2: Run test to verify it fails**
Run: `pytest tests/path/test.py::test_name -v`
Expected: FAIL with "function not defined"

**Step 3: Write minimal implementation**

```python
def function(input):
    return expected
```

**Step 4: Run test to verify it passes**
Run: `pytest tests/path/test.py::test_name -v`
Expected: PASS

**Step 5: Commit**

```bash
git add tests/path/test.py src/path/file.py
git commit -m "feat: add specific feature"
```
```

### 4. Key Principles
*   **Exact File Paths**: Always use absolute or relative paths from root.
*   **Complete Code**: Provide complete snippets, not "add validation here".
*   **TDD**: Always write tests first.
*   **DRY & YAGNI**: Don't repeat code; don't add features not asked for.

## Execution
After saving the plan to `docs/plans/`, ask the user if they want to proceed with execution.
