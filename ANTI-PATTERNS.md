# Anti-Patterns to Avoid

## 1. Building Directly in Public Repos
Never develop new skills, documentation, or plans directly in a public repository. Always use a private development repo first.

## 2. Skipping Timestamp Discipline
Filenames should follow `YYYY-MM-DD_HHMM_TZ_Description.md` format. This makes history easy to navigate.

## 3. Vague Commit Messages
Avoid messages like "updated files" or "fix stuff". Be descriptive.

## 4. Ignoring Connector-First Workflow
When possible, use the GitHub connector tools instead of local file creation + manual pushing.

## 5. Mixing Internal Concepts into Public Skills
Public skills should remain generalized. Do not leak internal processes, frameworks, or terminology into public repositories.