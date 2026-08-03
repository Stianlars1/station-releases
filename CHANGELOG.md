# Changelog

## 1.2.1 (17) - Fast startup readiness
_Date: 2026-08-03_

- Docker readiness checks no longer leave stack startup waiting after Docker is already available.
- Already-running configured Docker containers are accepted as ready dependencies only when the exact container and configured port are active.
- Per-app starting indicators now appear promptly instead of remaining visually stopped behind the stack progress banner.
- Finder-launched sessions now discover common Node toolchains without loading interactive shell prompts.

## 1.2.1 (16) - Reliable stack startup
_Date: 2026-08-03_

- Starting a stack now asks before stopping processes that occupy required ports, then revalidates each PID, port, and working directory before Station takes control.
- Configured Docker containers that are already running are adopted as healthy external dependencies instead of being reported as foreign port conflicts.
- Apps that share a working directory no longer create false port-mismatch errors for each other.
- Terminal sessions start at a usable width and no longer load interactive shell startup prompts, preventing broken line wrapping and blocked launches.
- Keeping a migrated setup is remembered across launches, and a previously exported app setup can now be imported directly during first-time setup.

## 1.2.0 (15) - Reliable runtimes and flexible setups
_Date: 2026-07-28_

- Fixed Docker detection for apps launched from Finder and added cancellable startup guidance when Docker is unavailable, slow, or not responding.
- Made grouped stop operations terminate Station-owned process groups, preserve genuinely shared or external services, and report per-app progress and outcomes.
- Added automatic local troubleshooting after runtime failures, with structured evidence and reviewable AI Doctor configuration proposals that are never saved without approval.
- Improved app details with labeled, selectable metadata, copy actions, Finder access, readable command formatting, and separate running and health states.
- Added nested drag-and-drop groups with recursive start and stop behavior.
- Added four deliberate dependency-display presets: pixel-aligned Trace, a calm curved Flow, line-free Signals, and line-free Highlights.
- Dependency relationships now stay anchored to the selected app, support both directions and right-to-left layouts, and scale with the app's text zoom without flickering between rows.
- Made the Settings window resizable and gave every pane a consistent size, so switching tabs no longer resizes the window and taller panes no longer need scrolling at a fixed height.
- Added a Settings notice when a locally built, unreleased version is running, explaining why update checks still report that Station is up to date.
- Added user-selected app setup export locations, visible saved paths, Finder reveal, and validated import with a replacement preview and confirmation.
- Added complete localization for the new runtime, troubleshooting, hierarchy, dependency, and setup-transfer experiences across all 14 supported languages.
- Kept XCTest hosts hidden and isolated from user catalogs and preferences, and corrected inspector sizing in right-to-left layouts.

## 1.1.4 (14) - Balanced sidebar search
_Date: 2026-07-20_

- The sidebar search field now follows the panel's rounded top edge with balanced spacing while retaining native live filtering, clearing, focus, and accessibility behavior.

## 1.1.3 (13) - Activation banner and installer privacy
_Date: 2026-07-20_

- The activation-required notice now reserves space above the sidebar, main view, and inspector instead of covering their content.
- Installer metadata no longer retains creator-local build paths.

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
