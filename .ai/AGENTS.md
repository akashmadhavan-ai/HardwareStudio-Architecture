# AI Agents Operating Guidelines & Workspace Rules

- **Project**: HardwareStudio Platform Architecture
- **Repository**: `HardwareStudio-Architecture`
- **Scope**: Engineering guidelines, AI responsibilities, and workflow rules for AI agents.

---

## Purpose

This document establishes the operational rules, engineering workflows, and collaboration boundaries for AI agents contributing to the HardwareStudio repository. It ensures that all AI agent interactions remain deterministic, transparent, aligned with project architecture, and compliant with repository standards.

---

## AI Operating Rules

1. **Strict Adherence to Engineering Standards**: AI agents must strictly follow the rules laid down in [001_PROJECT_VISION.md](file:///d:/HardwareStudio/HardwareStudio%20Architecture/HardwareStudio-Architecture/docs/001_Project/001_PROJECT_VISION.md), [002_PROJECT_GOALS.md](file:///d:/HardwareStudio/HardwareStudio%20Architecture/HardwareStudio-Architecture/docs/001_Project/002_PROJECT_GOALS.md), and [003_PROJECT_PHILOSOPHY.md](file:///d:/HardwareStudio/HardwareStudio%20Architecture/HardwareStudio-Architecture/docs/001_Project/003_PROJECT_PHILOSOPHY.md).
2. **Zero Unverified Mutations**: AI agents must not make unapproved changes outside the explicit task scope defined in `.ai/CURRENT_TASK.md`.
3. **No Implementation Details in Architectural Docs**: Early milestone documentation must focus purely on vision, goals, philosophy, problem statements, and requirements without leaking low-level software implementation choices.
4. **Deterministic Git Commits**: AI agents must perform requested Git workflows (`git add`, `git commit`, `git push`) accurately according to the specified task definitions.

---

## Engineering Workflow

Every engineering task follows a strict sequence:

```
Research → Analysis → Engineering Decisions → Document / Code Generation → Review → Freeze → Git Commit
```

- **One Active Task At A Time**: Only one task may be active in `.ai/CURRENT_TASK.md`.
- **Task Logging**: Upon completion of any task, `.ai/CURRENT_TASK.md`, `.ai/MEMORY.md`, and `.ai/TASK_HISTORY.md` must be updated before final Git operations.

---

## Coding Standards

When implementation code is introduced in later milestones:

- **Clean Code & Self-Documentation**: Write clear, self-explanatory code with strict type safety and domain-driven naming.
- **Contract-Driven Interfaces**: All modules must communicate across explicit interface boundaries.
- **Zero Warnings**: Maintain zero linter errors and zero build warnings.

---

## Documentation Standards

- **Standard Headers & Metadata**: All engineering documents must include Document Information (`ID`, `Title`, `Status`, `Version`, `Author`, `Dates`).
- **Markdown Formatting**: Use GitHub Flavored Markdown, proper heading hierarchy, and clickable relative markdown links for file paths.
- **Single Source of Truth**: Avoid duplicating specifications across multiple documents. Reference authoritative sources via explicit document links.

---

## Review Process

1. **Draft State**: New documents are authored with status `DRAFT` or `READY`.
2. **Verification & Audit**: Document content is audited against acceptance criteria, required sections, and engineering guidelines.
3. **Freeze Version 1.0**: Upon approval, the document status is changed to `Frozen` (Version 1.0).
4. **Version Control**: Changes are committed to Git with clear, conventional commit messages.

---

## AI Responsibilities

- Execute task instructions precisely as specified in task definitions.
- Author high-quality engineering documents following specified section structures.
- Keep `.ai/CURRENT_TASK.md`, `.ai/MEMORY.md`, and `.ai/TASK_HISTORY.md` up to date.
- Verify file locations and repository structures before making updates.

---

## Human Responsibilities

- Define task objectives, scope, and priorities.
- Review and approve frozen architectural documents and code changes.
- Provide domain guidance and resolve design ambiguities when requested.

---

## Repository Rules

- Do not create unrequested scratch files or clutter the root directory.
- Maintain empty directory tracking using `.gitkeep` files where necessary.
- Preserve repository layout and relative documentation links.
