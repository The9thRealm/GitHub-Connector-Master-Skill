# GitHub Connector Cheat Sheet

## Core Principles
- **Connector-First**: Always use the connector tools when possible instead of local file operations.
- **Timestamp Discipline**: Use `YYYY-MM-DD_HHMM_TZ` format in filenames.
- **Private-First Development**: Build in private repos first, then mirror to public.
- **Clean Commits**: Write clear, descriptive commit messages.

## Common Operations

### File Operations
| Action | Tool | Notes |
|--------|------|-------|
| Create/Update File | `github___create_or_update_file` | Most used tool |
| Get File Contents | `github___get_file_contents` | Read files remotely |
| Delete File | `github___delete_file` | Remove files cleanly |

### Branch & PR Management
| Action | Tool | Notes |
|--------|------|-------|
| Create Branch | `github___create_branch` | Create feature branches |
| Create Pull Request | `github___create_pull_request` | Open PRs programmatically |

### Issue Management
| Action | Tool | Notes |
|--------|------|-------|
| Create/Update Issue | `github___issue_write` | Full issue support with labels, assignees, milestones |
| Read Issue | `github___issue_read` | Retrieve issue details |

### Advanced
| Action | Tool | Notes |
|--------|------|-------|
| Search Commits | `github___search_commits` | Deep history search |
| Create Repository | `github___create_repository` | Programmatically create repos |

## Quick Timestamp Format
`2026-07-03_1430_PDT_filename.md` (include both PDT and UTC in body)