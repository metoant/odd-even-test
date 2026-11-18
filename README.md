# odd-even-test

A minimal test monorepo for experimenting with Changesets, GitHub Actions, and automated NPM releases.

## Packages

- `@odd-even-test/odd` — returns a random odd number
- `@odd-even-test/even` — returns a random even number

Both packages are versioned together using Changesets fixed versioning.

## Release flow

1. Make a change in a feature branch.
2. Run `pnpm changeset` and commit the generated `.changeset/*.md` file.
3. Open and merge a PR to `main`.
4. The Changesets bot opens a "Version Packages" PR.
5. Review and merge the "Version Packages" PR.
6. GitHub Actions publishes both packages to NPM and creates a GitHub Release.
