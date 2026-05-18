# Contribution Guidelines

## Issues

### External Contributions Must Address an Issue

If you are not internal to ASEI, your contribution must address an existing issue. If what you are hoping to contribute does not have an existing issue, then you are welcome to open an issue in accordance with the rules outlined below.

### Labelling

Issues must be labelled as one of the following:
* `bug` for bug reports.
* `enhancement` for feature requests or improvement to existing code.
* `documentation` for requesting new documentation or changes to existing documentation.

### Bug Reports

Bug reports **must** provide:
* A detailed description of the bug. Screenshots/recordings encouraged but not required.
* Platform details.
    * Operating system and version.
    * Kernel and version (if applicable).
    * Code editor (if applicable).
    * Hardware (if applicable).
    * Browser (if applicable).
* Minimal required steps to reproduce the issue.

## Branching

ASEI uses [Trunk Based Development](https://trunkbaseddevelopment.com/) for branching strategy in our VC.

### The `main` Branch

The `main` branch is reserved for the most up-to-date version of the code. If anybody wants a rolling release, they grab the software from the `main` branch.

### Development Branches

All work is done in ephemeral branches known as development branches. All development branches should be prefixed with one of the following:

* `bugfix/` for bug reports.
* `feature/` for new features.
* `enhancement/` for improvement to existing code.
* `documentation/` for new documentation or changes to existing documentation.

### Tagging

Tags in development branches should not be included in a PR to `main`.

Tags in `main` should follow every single pull request in accordance with [semantic versioning](https://semver.org/). In short, this takes the form of vX.Y.Z where X is incremented with the introduction of MAJOR changes, Y is incremented with MINOR changes, and Z is incremented with PATCHED changes.

For example, a software at version v1.0.0 gets a bugfix. It would then be v1.0.1. If it got a new feature, it would be v1.1.0. Note how the patch digit resets to 0. After so many MINOR increments (say, v1.12.0), you may decide it's now in a state that warrants a new MAJOR increment. This would now change to v2.0.0.

## Pull Requests

### Base Requirements

In most cases, pull requests must fulfill the requirements described below in order to be considered by ASEI reviewers.

* Must pass all automated tests.
* Must follow code style of the relevant existing codebase.
* Must directly address an issue.

### Title

The title must be in the format "[Label]: [Brief heading]" where `[Label]` is one of the main labels discussed in the [labelling section under Issues](#labelling). Examples:

* Enhancement: Updated touch panel driver code with debug flags
* Bugfix: Fixed button misalignment in settings menu UI
* Documentation: Added documenation for fuzzing tests

### Description

PR descriptions are required to include the following sections:

* **Minor changes** - A list of small changes made.
* **Major changes** - A list of major changes made.
* **Notes** - A small section with miscellaneous notes for the reviewer.

If there is nothing to be said for one of the above sections, leave the heading but put "Nothing of note" below. New PRs in American Sound repositories automatically populate with a baseline description. I recommend using this rather than writing your own, as it keeps things consistent.

### Reviews

If you are a community contributor, disregard. If you are a verified reviewer within the organization, this section applies to you. Before merging a PR, ensure that:

* All pipelines pass successfully or, in relevant cases, are re-written to run successfully.
* You have thoroughly reviewed every single change made within the PR and verified that nothing is implemented poorly or outside the required code style.
* The PR directly addresses an open issue.
* If AI is used in the contribution, that the contributor has made a genuine effort in their contribution and has not just mindlessly hacked AI slop into production code. While AI is fine if used correctly, lazy contributions are **unacceptable**.
