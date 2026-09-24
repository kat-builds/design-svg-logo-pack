# Repository Guidelines

## Purpose

This repository publishes one reusable Skill: `design-svg-logo-pack`.

The Skill inspects a target project's real product context, visual language, Design System, theme tokens, and brand-asset usage before creating or integrating logo, favicon, app-icon, PWA/maskable, and social-image assets.

The repository contains no application code.

## Skill Boundaries

The Skill must remain project-derived rather than template-driven.

Do not hard-code a universal:

- corner radius;
- rounded or square geometry;
- stroke weight;
- brand color;
- framework;
- asset path;
- metadata system;
- package manager.

When a target project already defines a Design System or theme/token source of truth, inspect and follow it. Use the Design System as visual context, not as product scope.

## Repository Structure

- `SKILL.md` — reusable workflow and boundaries.
- `agents/` — optional agent metadata.
- `references/` — supporting brief and legal-boundary guidance.
- `README.md` — public explanation and installation instructions.
- `LICENSE` — repository license.

If future versions add `assets/`, `scripts/`, or `tests/`, they are part of the Skill only when they are genuinely reusable and do not encode one project's visual answer.

## Public Repository Maintenance

Keep this repository self-contained for public users.

When updating the Skill, review `SKILL.md`, `agents/`, `references/`, and any future Skill-owned support folders together so relative references remain valid.

Repository-owned public documentation such as `README.md`, `AGENTS.md`, and `LICENSE` should be reviewed separately when behavior or installation guidance changes.

## Source Language

Maintain Skill source documentation in English unless a future locale system is intentionally added.

Keep examples generic and free of private project names, secrets, credentials, or environment-specific paths.

## Git Workflow

For meaningful public changes, use a working branch when practical and review the diff before merging.

Use specific commit subjects. Avoid vague messages such as `update`, `fix`, or `changes`.

## License

Keep the public Skill and its documentation compatible with the repository's Apache License 2.0.
