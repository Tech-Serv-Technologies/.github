# TechServ Standards and Templates Central Repo

Welcome to the central engineering hub for our organization. This repository houses global issue templates, development standards, and architectural guidelines shared across all team projects.

---

## Global Issue Templates

The templates found in the `.github/ISSUE_TEMPLATE/` directory are **automatically inherited** by all repositories within this organization. 

When opening an issue anywhere in our organization, please select the appropriate type:

*   **Bug Report (`fix:`)** - For reporting broken or unintended behavior in application logic.
*   **Feature Request (`feat:`)** - For proposing completely new features or business capabilities.
*   **Documentation Update (`docs:`)** - For correcting, expanding, or adding project documentation.
*   **Enhancement & Polish (`style:`)** - For minor UI updates, tweaks, or improvements to existing features.
*   **Code Refactoring (`refactor:`)** - For improving structural code health and cleaning technical debt.

---

## Development and Engineering Guides

Use the following links to review our global engineering processes, standards, and practices before contributing to code:

### Workflows & Git Standards
*   **[Conventional Commits Guide](./workflow-guides/conventional-commits.md):** Learn how to properly use `feat:`, `fix:`, and `style:` prefixes in your commit history.

---

## How to Add Project-Specific Templates

If a specific project requires an issue layout that deviates from these global defaults:
1. Create a `.github/ISSUE_TEMPLATE/` folder inside **that specific repository**.
2. Add your custom Markdown templates there.
3. This will cleanly override the global templates for that repository only.
