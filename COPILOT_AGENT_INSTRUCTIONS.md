# Copilot Coding Agent Instructions for This Repository

## 1. Overview
This repository uses the Copilot coding agent to automate code changes, reviews, and maintenance. The following instructions help the agent operate efficiently and safely in this codebase.

## 2. Code Style and Conventions
- **HTML:** Use 2 spaces for indentation. Prefer semantic HTML5 elements. Use double quotes for attributes.
- **JavaScript/TypeScript:** (If present) Use 2 spaces for indentation. Prefer `const`/`let` over `var`. Use ES6+ features where possible.
- **CSS:** (If present) Use 2 spaces for indentation. Prefer external stylesheets over inline styles.
- **General:** Follow the existing style of each file. If unclear, match the most common pattern in the repo.

## 3. Commit Message Guidelines
- Use clear, concise commit messages.
- Start with a verb in the imperative mood (e.g., "Add", "Fix", "Update").
- Reference related issues or PRs if applicable.

## 4. Pull Request Guidelines
- Group related changes in a single PR.
- Add a summary describing what and why.
- Ensure all changes are reviewed before merging.

## 5. Testing and Validation
- If adding or modifying code, ensure it works in a browser (for HTML/CSS/JS).
- If tests exist, run them before submitting changes.

## 6. Sensitive Files
- Do not commit secrets, credentials, or personal data.
- Do not modify `LICENSE` or `README.md` unless explicitly requested.

## 7. Documentation
- Update documentation if public interfaces or behaviors change.
- Keep `README.md` up to date with major changes.

## 8. Agent-Specific Instructions
- Prefer minimal, atomic changes unless a refactor is requested.
- Always explain the reasoning for non-trivial changes in PR descriptions.
- If unsure, ask for clarification in the PR or issue comments.

---

For more details, see [Best practices for Copilot coding agent in your repository](https://gh.io/copilot-coding-agent-tips).
