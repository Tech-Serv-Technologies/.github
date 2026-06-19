# Conventional Commits Standards Guide

This document outlines the organization-wide standards for commit messages and pull request titles. Adhering to these rules keeps our project history readable and enables automated changelog generation.

---

## Message Structure

Every commit message must follow this exact format:

```text
type(scope): description

[optional body]

[optional footer(s)]
```

*   **Type:** The intent of the commit (e.g., `feat`, `fix`, `style`). Must be lowercase.
*   **Scope (Optional):** The specific area of code changed, wrapped in parentheses (e.g., `auth`, `api`, `ui-button`).
*   **Description:** A short, imperative summary of the change. Do not capitalize the first letter, and do not end with a period.

---

## Allowed Commit Types

| Type | When to Use | Example |
| :--- | :--- | :--- |
| **`feat`** | Adding a completely new feature or user capability. | `feat(billing): add stripe webhook handler` |
| **`fix`** | Patching a bug or fixing broken production logic. | `fix(auth): resolve session timeout crash` |
| **`style`** | Layout, formatting, CSS tweaks, linting. No logic changes. | `style(sidebar): fix padding on mobile viewports` |
| **`refactor`** | Rewriting code to improve quality without changing behavior. | `refactor(users): simplify nested database queries` |
| **`docs`** | Changes made strictly to documentation, readmes, or guides. | `docs: update setup steps in main readme` |
| **`perf`** | Code changes optimized purely for speed or memory reduction.| `perf(images): compress homepage hero assets` |
| **`chore`** | Updating dependencies, build scripts, or project configurations.| `chore: upgrade react to version 19` |

---

## Breaking Changes

If a change breaks backward compatibility (API modifications, database drops, etc.), you must append an exclamation mark (`!`) after the type or scope, and explain it in the footer.

### Example:
```text
feat(api)!: remove support for v1 user endpoints

BREAKING CHANGE: The v1 endpoints are no longer supported. Clients must migrate to v2.
```

---

## Common Anti-Patterns to Avoid

*   **Vague descriptions:** `fix: fixed the thing` (Be descriptive).
*   **Capitalization / Punctuation:** `feat: Add new user profile.` (Use lower-case, no trailing period).
*   **Mixing types:** Using `feat:` when you actually only fixed a CSS color bug (that belongs under `style:`).
