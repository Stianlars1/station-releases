# Changelog

## 1.1.2 (12) - Deterministic startup failures
_Date: 2026-07-20_

- Apps that exit before becoming ready are now consistently marked as failed.
- Late terminal callbacks can no longer start dependents or overwrite a failed startup state.

## 1.1.1 (11) - Reliable shell startup
_Date: 2026-07-20_

- Fixed service and dependency startup on clean macOS accounts that do not yet have a readable `.zshrc` file.
- Shell configuration errors no longer prevent Station from launching the configured project command.

## 1.1 (10) - Safer project workflows
_Date: 2026-07-20_

- Added project discovery and atomic stack import for Node, Python, and Docker Compose projects.
- Added Quick Open with `Command-K` for apps, groups, views, and safe runtime commands.
- Added redacted support reports that can be reviewed, copied, or exported as Markdown or JSON from AI Doctor.
- Kept existing setups available for inspection when activation is required while locking edits, process control, and repairs.
- Added explicit confirmation and process identity checks before Station can stop external processes, while Global stop now preserves them.
- Added an evidence review step before AI Doctor sends redacted diagnostics to the configured provider and tightened repair boundaries.
- Fixed license activation, device linking, private server errors, and a Keychain read that could block the app during startup.
- Hardened checkout, webhooks, public license APIs, release metadata, and stable-release promotion against replay, stale events, and inconsistent state.
- Aligned the macOS app, website, localization catalog, and shared design system, including responsive navigation and clearer support guidance.

## 1.0 (9) - Polished installer
_Date: 2026-07-03_

- Shipped the hand-tuned DropDMG installer layout for the direct download.
- The DMG now mounts as `Station 1.0 (9)` so Finder does not reuse cached window geometry from earlier builds.
- The installer window shows only `Station.app` and the `Applications` drop target on the branded background.
- No app workflow changes are included in this build.

## 1.0 - Direct distribution launch
_Date: 2026-07-03_

- Released Station as a direct-distribution macOS app for macOS 14 and newer.
- Added the Command Center for apps, groups, and terminal sessions.
- Added port conflict detection, external process detection, HTTP checks, and port health checks.
- Added Dependency Matrix and Dependency Board with ordered start plans.
- Added Docker daemon control and governed AI Doctor diagnostics with approval-gated repairs.
- Added direct DMG download, a 7-day local trial, Paddle purchase, Clerk account center, and license activation for up to three Macs.
