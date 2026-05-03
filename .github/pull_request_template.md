<!-- Fill out every section. Delete the HTML comments before submitting. -->

## Summary

<!-- 1–3 sentences. What does this PR do, and why? -->

## Linked docs

<!-- Required for new packages or non-trivial features. Use `N/A` for typo fixes / chore PRs. -->

- RFC (if a strategic decision): `docs/rfcs/NNNN-<slug>.md`
- Spec (required for any package/component change): `docs/specs/<name>.mdx`
- Figma (required for any visual change): <paste Figma frame URL>

## Type of change

<!-- Tick one. The prefix on the PR title should match. -->

- [ ] `feat:` New feature (minor version bump)
- [ ] `fix:` Bug fix (patch version bump)
- [ ] `docs:` Documentation only
- [ ] `chore:` Tooling, deps, no behavior change
- [ ] `refactor:` Same behavior, cleaner code
- [ ] `test:` Tests only
- [ ] `BREAKING CHANGE:` (major version bump — explain in Summary)

## Checklist

- [ ] PR title follows Conventional Commits: `type(scope): subject`
- [ ] Branch follows naming convention: `type/short-slug`
- [ ] Linked the relevant RFC and/or spec (or marked `N/A` with reason)
- [ ] Updated the spec in this same PR if the public API or behavior changed
- [ ] `pnpm typecheck` passes locally
- [ ] `pnpm lint` passes locally
- [ ] `pnpm format:check` passes locally
- [ ] Added/updated a Changeset (`pnpm changeset`) if this affects a published package
- [ ] Self-reviewed the diff before requesting review

## Screenshots

<!--
Required for any PR that changes how a component looks or behaves on screen.
Delete this section only if the PR is non-visual (e.g. tokens-only schema change,
build tooling, docs typo).

For a NEW component, attach all of:
- Web (Chrome or Safari) — at least the default state, plus any new variants
- React Native — iOS simulator OR Android emulator (whichever the change targets;
  both if the change is cross-cutting)

For a BUG FIX, attach a "before" and an "after" screenshot for each affected platform.
-->

### Web

<!-- Paste screenshot(s) -->

### React Native (iOS / Android)

<!-- Paste screenshot(s). Note which simulator / device. -->

### Before / after (bug fixes only)

<!-- Two side-by-side screenshots: the broken state and the fixed state. -->

## Notes for reviewers

<!-- Anything reviewers should pay extra attention to, or context that's not obvious from the diff. -->
