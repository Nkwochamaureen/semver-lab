# How to Trigger a Release

The repository uses automated semantic versioning driven by commit messages on the `main` branch. The CI/CD pipeline inspects commit message prefixes to determine whether to create a patch, minor, or major release.

## Bug Fix (Patch Version)

To fix a bug or make a minor adjustment that doesn't add a new "feature," use the fix: prefix.
- Commit Message: fix: resolve login timeout on mobile
- Result: v1.0.0 → 1.0.1

## Feature Jump (Minor Version)

To add a new feature that is backward-compatible, use the feat: prefix. This will bump the middle digit of the version.
- Commit Message: feat: add user profile picture support
- Result: v1.0.1 → 1.1.0

##  Breaking Change (Major Version)
If a change requires users to update their own code or migrations, it is a breaking change.
- Commit Message: Use ! after the type or add BREAKING CHANGE: in the footer.
- Example: feat!: overhaul database schema for v2
- Result: v1.1.0 → 2.0.0

