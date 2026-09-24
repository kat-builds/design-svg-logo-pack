# Design SVG Logo Pack

A reusable Skill for creating and integrating a complete web brand asset pack from the project that already exists.

Instead of starting from a fixed logo style, the Skill checks the product context, current visual language, theme tokens, Design System, and the asset paths the site actually uses. It then creates the logo, favicon, app-icon, PWA/maskable, and social-image assets that are actually needed.

It does **not** assume the product should be rounded, sharp, monoline, bold, or any other preset style. The visual direction comes from the project.

## What It Does

The Skill can:

- inspect the current product and brand context;
- read the project's Design System when one exists;
- find the real logo, favicon, manifest, app-icon, and social-image usage points;
- derive logo geometry and colors from the project's visual language instead of imposing a template;
- create light/dark variants when the project needs them;
- generate the platform sizes actually referenced by the project;
- integrate the new assets into the existing repository paths;
- validate dimensions, contrast, favicon legibility, maskable safe areas, and asset references.

## Installation

### Shared personal Skills folder

If your coding agent supports `~/.agents/skills`, clone this repository directly into that folder:

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/kat-builds/design-svg-logo-pack.git ~/.agents/skills/design-svg-logo-pack
```

Then restart or reopen your coding agent if needed.

### Other agent-specific Skills folders

If your agent uses its own Skills directory, clone or copy the repository there instead.

For example:

```text
~/.claude/skills/design-svg-logo-pack
~/.gemini/skills/design-svg-logo-pack
```

Use the Skills location supported by your coding agent.

## Usage

Ask your coding agent to use the Skill when you want to create, refresh, recolor, resize, or integrate a product's brand assets.

For example:

```text
Use $design-svg-logo-pack to inspect this project and create the complete logo, favicon, app-icon and social-image asset set it actually needs.

Follow the current product context, Design System and theme instead of forcing a new visual style.
```

The Skill will inspect the project first. If an important branding decision is genuinely missing, it asks only for the minimum information needed before continuing.

## How It Chooses the Visual Direction

The Skill uses project evidence in this order:

1. explicit user direction;
2. current brand assets that are still valid;
3. the project Design System and theme tokens;
4. current UI and shared visual patterns;
5. product context from the PRD, config, or product copy;
6. a documented fallback only when the project has no usable visual direction.

That means one project can be mostly square, another can be rounded, and another can use mixed shapes. The Skill records and follows the project instead of deciding that every product should look the same.

## Repository Structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── legal-boundary.md
│   └── logo-brief-checklist.md
├── AGENTS.md
├── LICENSE
└── README.md
```

`SKILL.md` contains the reusable workflow. The reference files contain the brief and legal-boundary guidance used when relevant.

## License

Copyright 2026 Katrina Lin.

Licensed under the Apache License 2.0. See `LICENSE` for details.
