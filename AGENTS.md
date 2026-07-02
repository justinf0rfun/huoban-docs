# AGENTS.md

This repository contains the Mintlify source for Huoban docs.

## Mintlify source of truth

- Pages are MDX files with YAML frontmatter.
- Navigation, theme, logo, navbar, and site metadata live in `docs.json`.
- The production deployment is Git-driven from `justinf0rfun/huoban-docs` on `main`.
- Do not edit the hosted Mintlify editor as the source of truth when this Git repo is available.

## Mintlify component rules

- Prefer plain Markdown for normal prose.
- Use `CardGroup` and `Card` for entry points and feature summaries.
- Use `Steps` and `Step` only for ordered reading paths or workflows.
- Use fenced code blocks for commands and examples.
- Reuse existing MDX patterns in this repo before introducing a new component.
- Do not invent Mintlify component props.
- If a component prop is not already used in this repo, verify it against Mintlify official docs before using it.
- For `Card`, `type="tip"` is the approved light green card style in this site.
- For icon names, use known working Font Awesome icon names or existing icons already rendered in this site.

## Huoban writing rules

- Keep the public positioning sentence stable: `Huoban 是 AI 系统的开放编排协议：可排版、可润墨、可印刷。`
- Use `Huoban（Huó Bǎn）活板` when the page title needs pronunciation.
- Explain the design philosophy with: `Huoban 活板的设计哲学来自活字印刷术。`
- Do not mention internal competitive analogies in public docs.
- Do not describe Huoban as a harness.
- Prefer verifiable examples and commands over prose-only claims.

## Editing rules

- Make narrow, page-specific edits.
- Do not rewrite navigation or multiple pages unless explicitly requested.
- Before committing, run:

```bash
git diff --check
git status --short
```

- Commit and push only after confirming the diff is scoped to the request.
