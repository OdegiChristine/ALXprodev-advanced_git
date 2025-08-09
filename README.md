# Advanced Git Workflow Repository

## Overview
This repository demonstrates a complete **Git Flow** workflow and custom **Git hooks** for managing a multi-feature development process.  
It serves as a practical example of branching strategies, release management, and automated Git actions that help maintain repository quality and consistency.

---

## Repository Structure
The repository contains the following main directories:

- **`login-page/`** – Initial scaffolding for the login feature.  
  Contains a `README.md` with a placeholder message for upcoming functionality.

- **`signup-page/`** – Initial scaffolding for the signup feature.  
  Includes a `README.md` outlining planned data requirements for user registration.

- **`merge_log.txt`** – Automatically updated log file generated after merges into the `main` branch.

---

## Git Flow Integration
The repository is initialized with **Git Flow** using:
- **Main branch:** `main` – production-ready code.
- **Develop branch:** `develop` – integration branch for upcoming releases.
- **Feature branches:** `feature/implement-login`, `feature/implement-signup`.
- **Release branches:** e.g., `release/1.0.0`.

This structure ensures:
- Isolated feature development.
- Controlled releases.
- Consistent integration process.

---

## Custom Git Hooks
Two Git hooks are implemented for repository quality control:

1. **Pre-commit Hook**  
   - Checks every directory in the repository for a `README.md` file.  
   - Prevents commits if any directory is missing documentation.

2. **Post-merge Hook**  
   - Runs after a merge into the `main` branch.  
   - Logs the merge date, commit details, and branch information to `merge_log.txt`.

> **Note:** Hooks in `.git/hooks` are local to each clone of the repository and are **not** pushed to remote.  
> To share them across environments, they can be stored in a tracked folder and applied via `git config core.hooksPath`.

---

## Purpose
This repository can be used as:
- A learning resource for mastering Git Flow.
- A reference for setting up automated Git hook scripts.
- A starting point for projects requiring structured branching and release cycles.

---

## License
This repository is for educational purposes.  
You are free to clone, modify, and adapt it to suit your own workflows.
