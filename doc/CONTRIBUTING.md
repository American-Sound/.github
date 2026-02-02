# Contribution Guidelines

## Issues

### Labelling

Issues must be labelled as one of the following:
* `bug` for bug reports.
* `enhancement` for feature requests or improvement to existing code.
* `documentation` for requesting new documenation or changes to existing documenation.

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


## Pull Requests

### Base Requirements

In most cases, pull requests must fulfill the requirements described below in order to be considered by ASEI reviewers.

* Must pass all automated tests.
* Must follow code style of the relevant exisitng codebase.
* Must directly address an issue.

### Title

The title must be in the format "[Label]: [Brief heading]" where `[Label]` is one of the main labels discussed in the [labelling section under Issues](#labelling). Examples:

* Enhancement: Updated touchpanel driver code with debug flags
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
* You have thoroughly reviewed every single change made within the PR and verified that nothing is implemented poorly or outside of the required code style.
* The PR directly addresses an open issue.
* If AI is used in the contribution, that the contributor has made a genuine effort in their contribution and has not just mindlessly hacked AI slop into production code. While AI is fine if used correctly, lazy contributions are **unacceptable**.
