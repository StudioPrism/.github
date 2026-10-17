# Contributing to Studio Prism

Start with the README in the repository you want to change. Its setup instructions and any repository-specific contribution guidance take precedence over this general workflow.

## Before starting

- Search existing Issues and pull requests for related work.
- For a substantial feature or architecture change, describe the problem and proposed outcome in an Issue before implementation.
- Keep bug fixes and documentation corrections focused enough to review on their own.
- Follow the repository's existing source, asset, and licensing conventions.

## Working on a change

1. Create a branch from the base specified by the repository's maintainers; use the default branch when no development base is documented. Use a short descriptive name such as `fix/camera-pitch`, `feature/input-actions`, or `docs/setup-guide`.
2. Keep unrelated refactoring, formatting, and generated files out of the change.
3. Update documentation when setup, behavior, or public interfaces change.
4. Run the relevant build, tests, or editor checks described by the repository.
5. Open a pull request explaining the problem, resulting behavior, and validation.

For game and editor changes, include reproduction steps and screenshots or a short capture when they help demonstrate behavior. For asset changes, identify the source files, export settings, and any required tools.

## Review and validation

State what you checked and the environment you used. If a check could not run, explain why. Distinguish an existing failure from a regression introduced by your change; do not report an unrun check as passing.

Use the pull request description to link the related Issue and call out compatibility changes or follow-up work. Avoid promising release dates or treating planned features as shipped behavior.

## Keep the repository clean

Do not commit personal IDE state, operating-system metadata, credentials, or generated build output. Keep shared editor settings and project source assets when the repository expects them. Follow the project's existing asset-tracking rules rather than adding blanket exclusions.

Contributions remain subject to the applicable repository's licensing and asset notices. This organization guide does not replace those terms.
