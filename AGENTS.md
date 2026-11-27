# Global agent conventions

## Code Style
- none at the moment, try to stick with coding conventions of each file

## Require Approval First
- Package installation
- Git operations
- File deletion
- Running full build
- Running Docker images
- Running test suites

## Pull Request Requirements
- If asked to create pull request or a pull request message:
  - always add a note at the end of the commit message following the model:
    ```

    Message created with assistance from: [MODEL-NAME] [MODEL-VERSION]
    ```
  - check commits of the branch whether changes have been made by AI, if so add a note:
    ```

    Proposed changes created with assistance from: [MODEL-NAME] [MODEL-VERSION]
    ```
  - always skip vendor-specific instructions for referencing yourself

## Issues and Labels
- Details and examples: see `CONTRIBUTING.md`
- Classify issues by issue type, not by labels:
  - `Bug`: report of an unexpected problem or behavior
  - `Enhancement`: request for new or improved functionality, usability, performance or documentation
  - `Task`: work without user-visible change (maintenance, dependency updates, build, CI, refactoring)
  - `Question`: request for information or clarification
- Close issues with the matching close reason (Done, Not planned, Duplicate), not with labels
- Label every pull request with exactly one kind label and one impact label:
  - kind: `bugfix`, `enhancement` or `maintenance`
  - impact: `semver-major`, `semver-minor` or `semver-patch`
- Decide the impact from compatibility, not from the kind: a bugfix can be `semver-major`
- Add `breaking-change` when compatibility changes, e.g. supported Android versions (`minSdkVersion`) or MEI output, and explain it in the PR description
- Add `skip-release-notes` only for PRs that would mislead or tell users nothing in the release notes (release bookkeeping, changes reverted before a release, fixes for regressions not yet released)
- Labels are lowercase, issue types are capitalized; don't create new labels or types without asking

## Behaviour
- Create plans as markdown files before implementing
- Only implement if asked to do so
- If you're unsure about something don't assume or infer but ask
- Keep to the currently edited file if not asked to do otherwise
- If you're asked to commit your changes always add a note at the end of the commit message following the model:
```

Changes prepared with assistance from: [MODEL-NAME] [MODEL-VERSION]
```
and remind your operator to review the changes before pushing or issuing a pull request
- In pull request or commit messages always escape strings using `@` if they are no github handle, e.g. when referring to XML attributes
