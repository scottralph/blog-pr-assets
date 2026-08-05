# blog-pr-assets

Public host for screenshots referenced from issues and pull requests in the (private) `scottralph/website` repo.

GitHub can't inline-render images that live in a private repo (committed files, or raw URLs pointing back into it) — its image proxy can't authenticate on a viewer's behalf. Screenshots hosted here, in a **public** repo, render fine via `raw.githubusercontent.com` regardless of the referencing issue/PR's privacy.

## Adding an image

1. Clone this repo.
2. Add your file(s) using the naming convention below.
3. Commit and push to `main`.
4. Reference it from the issue/PR body as:
   ```
   ![before](https://raw.githubusercontent.com/scottralph/blog-pr-assets/main/issue-<N>-before.png)
   ```

## Naming convention

- Before/after pair for a code change: `issue-<N>-before.png` / `issue-<N>-after.png`
- Anything else (a design concept, a mockup, a one-off illustration): `issue-<N>-<short-description>.png`

`<N>` is the GitHub issue number the image supports — even if what you're actually attaching it to is a PR, name it after the *issue* the PR closes, so it's easy to find later.

## Never delete a file from this repo

This is the one rule that matters. A file here can be linked from an issue comment or a **merged** PR that's part of the permanent project history — there's no reliable way to know every place a given URL is referenced short of searching all of `scottralph/website`'s issues and PRs (open *and* closed) for it, and a rushed check is exactly how a real image got deleted here once already (see the manifest below — `issue-5-*` and `issue-13-*` were briefly deleted by an agent following an earlier version of this README that said to "prune old images," then had to be restored).

There is no pruning step in this workflow anymore. Storage is not a real constraint here: a personal blog's PR screenshots, even after years of activity, won't approach a size where a handful of small PNGs matters. If that ever genuinely changes, that's a deliberate future decision to make with full visibility into what's still referenced where — not a routine step baked into every new PR.

**If you (human or agent) ever think a file here looks stale and want to remove it anyway:** don't. Ask first.

## Current files

| File | Referenced by |
|---|---|
| `issue-5-before.png` / `issue-5-after.png` | PR #14 (merged) |
| `issue-13-favicon-concept.png` | Issue #13, design-approval comment |
| `issue-13-before.png` / `issue-13-after.png` | PR #15 (merged) |
| `issue-6-before.png` / `issue-6-after.png` | PR #17 (open) |

Keep this table current when you add a file — it's the fast way to check "is this still needed" without a search.
