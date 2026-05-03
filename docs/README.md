# Bloom — Documentation

Every package and component in Bloom has a written spec. **If a non-trivial change ships without an updated spec, that's a bug.**

New here? Start with [`workflow.md`](./workflow.md) — how design and engineering collaborate on Bloom.

## Layout

```
docs/
├── README.md             ← you are here
├── workflow.md           ← how we work
├── templates/            ← copy these to start a new doc
│   ├── rfc.md
│   └── spec.mdx
├── rfcs/                 ← cross-cutting "should we do this?" decisions
└── specs/                ← one .mdx per package or component
```

## The two document types

|                   | RFC                                                 | Spec                                             |
| ----------------- | --------------------------------------------------- | ------------------------------------------------ |
| **Lives in**      | `docs/rfcs/`                                        | `docs/specs/`                                    |
| **Format**        | `.md`                                               | `.mdx` (live examples once Storybook is wired)   |
| **Answers**       | _Should we do this? What did we consider?_          | _What is it, how does it work, how do I use it?_ |
| **Lifecycle**     | Written once, rarely edited after merge             | Living — updated in the same PR as code changes  |
| **Status field**  | Draft → Proposed → Accepted / Rejected / Superseded | Alpha → Beta → Stable                            |
| **When to write** | Before deciding to build something non-trivial      | Before / during implementation, then forever     |

### When does something need an RFC?

Write an RFC when the decision is **strategic and cross-cutting** — it affects more than one package, sets a precedent, or has reasonable alternatives worth recording.

Examples:

- "Should we adopt the DTCG token spec?"
- "Should our build emit ESM only, or ESM + CJS?"
- "How do we handle theming on React Native?"

We **don't** need an RFC for:

- Adding a single component (the spec covers it)
- Bug fixes
- Refactors with no public API change

### What goes in a Spec?

The spec template has 19 sections covering: API, anatomy, variants, states, behavior, accessibility, cross-platform parity, tokens consumed, architecture, implementation, performance, testing, design decisions, versioning, and references.

For non-component packages (tokens, utils, hooks), some sections are N/A — the template tells us which to drop.

## Naming conventions

| Type | Path                               | Example                                |
| ---- | ---------------------------------- | -------------------------------------- |
| RFC  | `rfcs/NNNN-<slug>.md`              | `rfcs/0001-tokens-package.md`          |
| Spec | `specs/<package-or-component>.mdx` | `specs/tokens.mdx`, `specs/button.mdx` |

RFC numbers are monotonically increasing and never reused, even for rejected RFCs.

## Status of an RFC

Every RFC carries one of these statuses in its frontmatter table:

- **Draft** — being written, open for discussion
- **Proposed** — PR open, awaiting review
- **Accepted** — merged; implementation can begin
- **Rejected** — explicitly turned down (kept as a record so we don't re-litigate)
- **Superseded by RFC NNNN** — replaced by a later RFC

## Status of a Spec

- **Alpha** — API may change without notice. Not for production.
- **Beta** — API mostly stable; breaking changes go through a deprecation cycle.
- **Stable** — Semver-protected. Breaking changes require a major bump and migration guide.

## Index

<!-- Update this when an RFC or spec is merged. -->

### RFCs

_None yet._

### Specs

_None yet._
