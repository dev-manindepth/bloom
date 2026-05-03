# Bloom — Documentation

Every package and component in Bloom has a written spec. **If a non-trivial change ships without an updated spec, that's a bug.**

New here? Start with [`workflow.md`](./workflow.md) — how designers and engineers collaborate on Bloom.

## Layout

```
docs/
├── README.md
├── workflow.md
├── templates/
│   ├── rfc.md
│   └── spec.mdx
├── rfcs/
└── specs/
```

- `workflow.md` — how designers and engineers collaborate on Bloom.
- `templates/` — copy from here to start a new RFC or spec.
- `rfcs/` — decisions that affect more than one package or establish a pattern others will follow.
- `specs/` — one MDX per package or component, covering API, behavior, and design decisions.

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

Write an RFC when any of these apply:

- The decision affects more than one package.
- It will become a pattern that future components or packages copy.
- There's more than one reasonable way to do it, and we want a written record of why we chose this one.

Examples that need an RFC:

- "Should we adopt the DTCG token spec?"
- "Should our build emit ESM only, or ESM + CJS?"
- "How do we handle theming on React Native?"

Examples that don't:

- Adding a single component (the spec covers it).
- Bug fixes.
- Refactors with no public API change.

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
