# Website collection installation in v0.12.0

[简体中文](website-collection-install.zh.md) · [PR #185](https://github.com/qufei1993/skills-hub/pull/185)

## Installation flow

Open a collection on the website to review its Skills and sources in Skills Hub. A collection can contain Skills from one GitHub repository or combine several authors' repositories, each pinned to a specific commit.

Opening a link only validates and displays the request. Installation starts after confirmation. Skills are added to the shared library, with optional global distribution to selected tools; no tools are selected by default. Existing same-source Skills remain unchanged, conflicts are reported, and failed items can be retried without reinstalling successful items. Failed tool distribution can resume without reinstalling the Skill.

An idle manual Add Skill view closes to show the collection confirmation while preserving its form values. Active operations and other confirmations finish before the collection dialog opens. Temporarily deferred confirmation retains installation and retry progress, and repository candidate paths match across Windows and Unix directory separators.

## Desktop launch and platform support

Protocol registration ships in the desktop installer; users of older versions need to update to v0.12.0 or later.

- **macOS**: Valid links show, restore, and focus the main window, including when the app is already running or minimized. Invalid links do not activate it. A development process alone does not register the URL scheme; use a bundled app to verify OS-level launch.
- **Windows and Linux**: The single-instance plugin forwards links to the running window. Scheduled background update processes bypass the single-instance lock. Debian installers include protocol-registration utilities; registration failures do not prevent desktop startup, and package startup verification uses an isolated desktop bus session.

## Link contract and installation safeguards

Website links use `skills-hub://install?manifest=<encoded JSON>`. Manifest v1 contains a collection title, GitHub sources pinned to 40-character commit hashes, and selected Skill names and directories.

The parser rejects unsupported versions, unsafe paths, credentials, extra parameters, duplicate entries or names, unpinned sources, and oversized requests. Receiving a link performs no network or credential access. Confirmed installation uses existing services, operation locks, and proxy-aware Git commands. No database migration is required.
