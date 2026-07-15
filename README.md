# Huoban documentation

This repository contains the Mintlify source for the Huoban documentation site.

Huoban 是 AI 系统的开放编排协议：可排版、可润墨、可印刷。

## Source of truth

- Protocol schemas, CLI behavior, and executable examples live in the `huoban` source repository.
- Public documentation pages and navigation live in this repository.
- Production deploys from `main` through the Mintlify Git integration.

When protocol behavior changes, update the source repository first, then update the corresponding model page, specification page, example, glossary entry, and changelog here.

## Local development

Use Node.js 20.17 or later.

```bash
npx mintlify dev --port 3333
```

Open `http://localhost:3333`.

## Validation

Run all documentation checks before committing:

```bash
npx mintlify validate
npx mintlify broken-links
npx mintlify a11y
git diff --check
```

## Publishing

Push reviewed commits to `main`. Mintlify builds and publishes the Git-backed deployment automatically; the hosted editor is not the source of truth.
