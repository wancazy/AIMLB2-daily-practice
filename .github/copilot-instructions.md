<!-- .github/copilot-instructions.md - Guidance for AI coding agents working in this repo -->

# Agent Instructions — AIMLB2-daily-practice

Summary
- This repository is a lightweight daily-practice collection (not a deployed app). Work is organized by day/lesson folders (e.g. `Day 6 - Modules & Library numpy/`). Primary contents are small Python scripts and Jupyter notebooks used for learning exercises.

What to expect
- Flat, lesson-focused structure: each day folder contains one or more notebooks and supporting `.py` files. Example: `Day 6 - Modules & Library numpy/numpy.py` and `Day 6 - Modules & Library numpy/learn lib.jpynb`.
- No build system, CI config, or test framework present in the repository root. There are no package manifests (`requirements.txt` / `pyproject.toml`) detected.

Big-picture architecture (for an agent)
- Purpose: personal practice / learning — changes should be minimal and educational. Prefer small, well-explained edits rather than large refactors.
- Data flow / integration: there are no services or external integrations. Code is local and self-contained in lesson folders.

Developer workflows & commands
- Run a notebook locally with Jupyter:
  - `python3 -m notebook` or `jupyter lab`
- Run a standalone lesson script:
  - `python3 "Day 6 - Modules & Library numpy/numpy.py"`
- If you add dependencies, include a `requirements.txt` at repo root and document how to create a venv:
  - `python3 -m venv .venv && source .venv/bin/activate && pip install -r requirements.txt`

Project-specific conventions
- Folder naming: days use a leading `Day N -` prefix and may contain spaces; always wrap paths in quotes when running in shell.
- Notebooks: keep notebooks small and self-contained. When converting notebook examples to scripts, place them in the same day folder and name with a clear suffix (e.g. `example_from_notebook.py`).
- Minimal changes: this repo is a learning journal — prefer to add new files rather than change historical content unless correcting errors. When editing existing lesson files, include a short comment at the top with the reason for the change.

Guidance for generating code changes (actionable rules)
- Make tiny, well-scoped edits. Each patch should only touch files necessary to implement the change.
- Use the repository's existing style: simple procedural Python, no new frameworks unless requested.
- When adding dependencies, add `requirements.txt` and document `pip` steps in the repository README.
- Avoid creating complex infrastructure (no Docker, no CI) without explicit user request.
- Prefer adding a short example script that demonstrates how to run any new feature.

Examples from the codebase
- To show how modules are organized, look at `Day 6 - Modules & Library numpy/numpy.py`. If you add or modify modular code, follow the same simple import patterns and minimal function-level encapsulation.

What this agent should NOT do
- Do not perform large-scale refactors or rename many files across multiple day folders.
- Do not introduce external services, authentication, or networked backends.

When uncertain
- Ask the repo owner for clarification before making breaking changes or adding new build tooling.

Change log for this file
- Created to provide concise, codebase-specific direction to AI agents working on this repository.

Please review and tell me if you want more detail (examples, preferred commit message templates, or a small README update).
