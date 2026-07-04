# GitHub Connector Master Skill

**Version:** 1.0  
**Type:** Portable Master Skill (Generalized)  
**Compatibility:** Grok (Cloud, iOS, Web, CLI), Claude (Desktop, iOS, Web), and any platform that supports loading `.md` skill files.

---

## Positioning & Purpose

This is a **portable master skill** designed to give any AI agent comprehensive understanding and operational mastery of the GitHub connector's advanced capabilities.

**Important:**
- This is a **skill**, not an MCP server itself.
- It is designed to be loaded **after** you already have a working GitHub connector/MCP installed.
- It contains no framework-specific processes, terminology, or dependencies.
- The goal is to enable any agent to use the GitHub connector at a high, professional level across multiple environments.

---

## Core Principles

### 1. Connector-First Workflow
Always prefer using the GitHub connector tools directly rather than creating files locally first. This maintains clean git history and follows best practices.

### 2. Timestamp Discipline
Use explicit, consistent timestamps in filenames and document bodies. Format: `YYYY-MM-DD_HHMM_TZ` (e.g., `2026-07-03_1415_PDT`). Always include both local time and UTC when relevant.

### 3. Clean Commit Standards
Every commit should have a clear, descriptive message. Use conventional commit style when appropriate (`feat:`, `fix:`, `docs:`, `handoff:`, etc.).

### 4. Repository Hygiene
When working in a target repository (especially during migrations or large changes), follow "minimal noise" principles — only add essential, well-structured files.

### 5. Review Before Public
Never build directly in a public repository. Always develop in a private repository first, then switch to public or create a clean public mirror after review.

---

## Full Capability Encyclopedia

### File Operations
- `create_or_update_file`: Create new files or update existing ones with full content control.
- `delete_file`: Remove files from a repository.
- `get_file_contents`: Retrieve file or directory contents (supports specific refs/SHAs).

### Branch Management
- `create_branch`: Create new branches from existing ones. Supports specifying source branch.

### Pull Requests
- Create, update, and manage pull requests programmatically.
- Update PR base branch when needed.

### Issue System (Advanced)
The issue system is one of the most powerful parts of the connector:
- Create and update issues with rich metadata.
- Assign labels, assignees, and milestones.
- Set custom issue fields (single-select, text, number, date).
- Mark issues as duplicates.
- Change issue state with reason (`completed`, `not_planned`, `duplicate`).
- Full support for issue types when enabled on the repository.

### Sub-Issue Management
- Add, remove, and reprioritize sub-issues under a parent issue.
- Useful for breaking down complex work into structured hierarchies.

### Commit Inspection & History
- `get_commit`: Retrieve detailed commit information, including stats and full patch diffs.
- `search_commits`: Powerful search across repositories using GitHub's commit search syntax (author, date ranges, message content, etc.).
- Useful for archaeology, auditing changes, or finding specific implementations.

### Repository Management
- `create_repository`: Create new public or private repositories programmatically.
- Supports initialization with README and description.

### Projects (Advanced)
Full support for GitHub Projects:
- Create and manage projects, items, statuses, and iterations.
- Automate project workflows.

### Security & Scanning
- Access Dependabot alerts, Secret Scanning, and Code Scanning results.
- Useful for security monitoring and compliance workflows.

### Other Capabilities
- Releases and tags management
- Collaborator and permission management
- Workflow and Actions inspection
- Gist creation (public and secret)

---

## Quick Reference Cheat Sheet

| Operation                    | Tool                        | Common Use Case                          |
|-----------------------------|-----------------------------|------------------------------------------|
| Create/Update File          | create_or_update_file       | Adding docs, skills, handoffs            |
| Delete File                 | delete_file                 | Cleaning up old files                    |
| Get File Contents           | get_file_contents           | Reading existing files before editing    |
| Create Branch               | create_branch               | Feature work, safe experimentation       |
| Create Issue                | issue_write (method=create) | Task tracking, bug reports               |
| Update Issue                | issue_write (method=update) | Changing status, adding details          |
| Search Commits              | search_commits              | Finding when something was changed       |
| Get Commit Details          | get_commit                  | Reviewing exact changes in a commit      |
| Create Repository           | create_repository           | Bootstrapping new projects               |

---

## Best Practices

- Always use the connector for file operations when possible instead of local creation + manual push.
- Use descriptive, timestamped filenames for handoffs, investigations, and status documents.
- Keep commit messages clear and actionable.
- When migrating or reorganizing large repositories, follow a "private dev first, then public mirror" approach.
- Leverage the issue system for complex, multi-step work — it supports rich metadata and sub-issues.
- Use commit search when you need to understand history or find previous decisions.

---

## Anti-Patterns to Avoid

- Creating files locally in `/artifacts` or similar folders and then manually copying them (loses clean git history).
- Building directly in public repositories without review.
- Using vague commit messages (e.g., "update files").
- Ignoring timestamp discipline on important documents.
- Treating the GitHub connector as only a file writer — it has much deeper capabilities (issues, commits, projects, security).

---

## How to Use This Skill

Load this skill file into your agent. Once loaded, the agent should:
1. Prefer connector tools over local file creation.
2. Use timestamped naming for documents.
3. Write clear commit messages.
4. Leverage advanced features (issues, commit search, sub-issues, etc.) when appropriate.
5. Follow the Private-First Development Rule for any work that may eventually become public.

---

**This skill is designed to be self-contained and portable across environments.**