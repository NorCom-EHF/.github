# Contributing to NorCom EHF

Thank you for your interest in contributing to NorCom EHF projects! This document outlines the process and standards we follow across all repositories in the organisation.

> **Canonical source:** The authoritative version of this file is maintained in **NorCom.Engineering**. The copy in this repository is the active default surfaced to all NorCom-EHF repositories on GitHub.

---

## Table of Contents

1. [Code of Conduct](#code-of-conduct)
2. [Getting Started](#getting-started)
3. [Branching Strategy](#branching-strategy)
4. [Commit Messages](#commit-messages)
5. [Pull Requests](#pull-requests)
6. [Coding Standards](#coding-standards)
7. [Reporting Issues](#reporting-issues)

---

## Code of Conduct

All contributors are expected to treat each other with respect. Be professional and constructive in all interactions.

---

## Getting Started

1. Fork or clone the relevant repository.
2. Install required tools and dependencies as described in the repository's `README.md`.
3. Create a feature branch from `main` (see [Branching Strategy](#branching-strategy)).
4. Make your changes, following the coding standards below.
5. Open a pull request and fill in the PR template.

---

## Branching Strategy

| Branch prefix | Purpose |
|---|---|
| `feature/<short-description>` | New features |
| `fix/<short-description>` | Bug fixes |
| `chore/<short-description>` | Maintenance, refactoring, dependency updates |
| `docs/<short-description>` | Documentation-only changes |
| `release/<version>` | Release preparation |

- Branch off from `main`.
- Keep branches short-lived; open a PR as soon as meaningful work is ready for review.

---

## Commit Messages

Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(optional scope): <short summary>

[optional body]

[optional footer(s)]
```

**Types:** `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`, `ci`

Examples:
```
feat(sales): add blanket order consolidation
fix(finance): correct VAT rounding on credit memos
docs: update CONTRIBUTING with branching strategy
```

---

## Pull Requests

- Fill in all sections of the [PR template](pull_request_template.md).
- Every PR must reference at least one issue.
- At least **one approval** from a team member is required before merging.
- All CI checks must pass before merging.
- Use **Squash and Merge** for feature branches; use **Merge Commit** for release branches.

---

## Coding Standards

### AL (Business Central)

- Follow the [AL Guidelines](https://alguidelines.dev/) published by the community.
- Use `PascalCase` for object names, procedures, and variables.
- Prefix all custom objects and fields with the assigned object range prefix (see project-specific README).
- Write XML documentation comments on all public procedures.
- Avoid using `Commit` inside transactions unless absolutely necessary; document why when used.

### General

- No secrets, API keys, or credentials in source code — use Key Vault or environment variables.
- Write tests for new logic (unit tests and/or integration tests as appropriate).
- Keep PRs focused; avoid bundling unrelated changes.

---

## Reporting Issues

Use the appropriate issue template when opening a GitHub issue:

- **Bug Report** — reproducible defects
- **Feature Request** — new functionality or improvements
- **Copilot Task** — tasks to be delegated to GitHub Copilot Coding Agent

For security vulnerabilities, please follow the [Security Policy](SECURITY.md) and **do not** open a public issue.
