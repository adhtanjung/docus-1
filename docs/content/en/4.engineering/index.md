---
title: Technical Workflow
description: End-to-end engineering and AI-assisted development standards.
---

# Technical Workflow Documentation

This section defines the end-to-end technical workflow from **code creation → pull request → review → CI → merge → release**. These standards apply to **human-written and AI-generated code equally**.

## Purpose & Scope

### What This Document Governs

- All source code contributions to the HAER platform.
- The entire software development lifecycle (SDLC) from ideation to production release.
- Integration of AI-assisted coding tools into the engineering process.

### Who Must Follow It

- **Core Engineers**: Full-time development team members.
- **Reviewers**: Anyone with code approval responsibilities.
- **Contractors & Contributors**: External parties contributing to the codebase.
- **AI-Assisted Contributors**: Anyone using AI tools (Copilot, Claude, etc.) to generate code.

### Problems This Prevents

- **Unreliable AI Code**: Hallucinations, over-engineering, or subtle bugs from LLM outputs.
- **Large PRs**: Unmanageable pull requests that are impossible to review effectively.
- **Unclear Ownership**: Ambiguity about who is responsible for a piece of code.

---

## Development Workflow Overview

The high-level flow for any code change follows these steps:

::steps
### 1. Issue / Task Created

Work begins with a tracked issue (e.g., Jira, Linear, GitHub Issue).

### 2. Local Development

Engineer (with or without AI assistance) writes the code locally.

### 3. Pre-Commit Checks

Local linting, formatting, and type-checking must pass before committing.

### 4. Pull Request Creation

A PR is created targeting the appropriate branch.

### 5. Code Review & Approval

Human reviewers assess the change for correctness, security, and maintainability.

### 6. CI Validation

Automated tests, builds, and security scans must pass.

### 7. Merge & Release

Approved PRs are merged and deployed according to the release cadence.
::

---

## Production-Grade Software Characteristics

All contributions should aim to meet the following quality bar:

| Characteristic   | Description                                                              | Key Measures                                                |
| :--------------- | :----------------------------------------------------------------------- | :---------------------------------------------------------- |
| **Correct**      | Behaves as intended; edge cases handled; no regressions.                 | Test pass rate \~100%; high mutation score.                 |
| **Testable**     | Design supports unit, integration, and E2E testing.                      | Unit coverage > 90%; no flaky tests.                        |
| **Maintainable** | Readable, modular, and consistent for future contributors.               | Low cognitive complexity; idiomatic style.                  |
| **Scalable**     | Designed with performance, security, and operational robustness in mind. | Baseline benchmarks; graceful degradation.                  |
| **Diagnosable**  | Provides enough instrumentation for troubleshooting.                     | Structured logs; alert coverage for key paths.              |
| **Disciplined**  | Follows sound engineering practices (VCS, CI, static analysis).          | CI-gated commits; clean lint runs; no critical SAST issues. |

---

## Section Contents

Explore the detailed guides for each aspect of the workflow:

::card-group
  :::card
  ------

  icon: i-lucide-git-branch
  title: Branching Strategy
  to: /en/engineering/branching

  Source control, branch naming, and merge rules.
  :::

  :::card
  ------

  icon: i-lucide-bot
  title: AI-Assisted Policy
  to: /en/engineering/ai-policy

  Rules for using AI tools responsibly and effectively.
  :::

  :::card
  ------

  icon: i-lucide-git-pull-request
  title: Pull Request Rules
  to: /en/engineering/pull-requests

  PR size limits, structure, and mandatory fields.
  :::

  :::card
  ------

  icon: i-lucide-users
  title: Code Review
  to: /en/engineering/code-review

  Review requirements, focus areas, and approval workflow.
  :::

  :::card
  ------

  icon: i-lucide-check-circle
  title: CI & Automation
  to: /en/engineering/ci-automation

  Required checks, merge gates, and automation strategy.
  :::

  :::card
  ------

  icon: i-lucide-test-tube
  title: Testing Strategy
  to: /en/engineering/testing

  Test types, coverage expectations, and AI-generated code testing.
  :::
::
