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

## Maintained Source & Public Mirror

The maintained private source is:

```text
ai-config/.agents/skills/design-svg-logo-pack/
```

This public repository mirrors the reusable Skill files at repository root:

```text
SKILL.md
agents/
references/
assets/      # when present
scripts/     # when present
tests/       # when present
```

Do not overwrite repository-owned files during a Skill sync:

```text
README.md
AGENTS.md
LICENSE
```

When the Skill contract changes, update public documentation separately if the user-facing explanation or installation steps also need to change.

## Sync Checklist

When syncing from the maintained source:

1. copy only the Skill-owned paths;
2. review the complete diff;
3. confirm no private or environment-specific content was introduced;
4. verify references and relative paths still resolve from the public repository root;
5. update README only when the public behavior or usage changed;
6. commit with a message that describes the actual Skill change.

## Source Language

Maintain Skill source documentation in English unless a future locale system is intentionally added.

Keep examples generic and free of private project names, secrets, credentials, or environment-specific paths.

## Git Workflow

For meaningful public changes, use a working branch when practical and review the diff before merging.

Use specific commit subjects. Avoid vague messages such as `update`, `fix`, or `changes`.

## License

Keep the public Skill and its documentation compatible with the repository's Apache License 2.0.
