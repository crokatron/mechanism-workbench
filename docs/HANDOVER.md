# Mechanism Workbench: maintainer handover

[One-screen summary](START-HERE.md) · [User manual](USER-MANUAL.md) · [Feature overview](../README.md) · [Recorded validation](../VALIDATION.md)

## Purpose and behaviour to preserve

Explore a library of mechanical relationships with editable inputs, diagrams and explicit equations. The workspace includes linkages, levers, pulleys, rotary and linear mechanisms, fluid systems, springs and hydraulic door arrangements. It supports first-pass comparison and explanation rather than replacing a complete machine design.

- **Library and search:** Twenty-four built-in mechanisms grouped by category. (Interactive workspace.)
- **Equations and assumptions:** Inspect the model behind a result instead of relying on an unexplained output. (Interactive workspace.)
- **Linkage Studio:** Enter the dedicated linkage-design workspace from the library. (Interactive workspace.)
- **Door designer:** Adjust four-bar geometry, cylinder mounting and door clearance through motion. (Interactive workspace.)
- **Stress & strain:** Use sizing loads in the related stress checks. (Interactive workspace.)
- **Local defaults and exports:** Edit/save defaults, export/import a workspace and export door motion CSV. (Interactive workspace.)

The [demo](../demo.html) is a smaller, labelled simulation with fictional data. It explains cause and effect without the real service; it is not evidence of a working production installation. Numbered screenshots in the user manual distinguish actual-app captures from demo captures.

## Files and sources of truth

| Actual package path | Maintainer role |
| --- | --- |
| [external-sources/StandaloneTools/mechanism-workbench.html](../external-sources/StandaloneTools/mechanism-workbench.html) | Single-file workbench and example library |
| [demo-source](../demo-source) | Editable demo HTML/CSS/runtime and embedded screenshot tour |
| [SOURCE-MANIFEST.json](../SOURCE-MANIFEST.json) | Original copied-source paths and SHA-256 checkpoint values |

The original working source is under C:/Users/lamon/Desktop/AI TOOLS/NAS for NAS modules; adjacent CAD/watch source locations are recorded by the full backup’s reviewed source manifest. This package contains only the explicitly copied source, not an automatic mirror. The main private nas-projects backup retains the broader shared host context.

## Setup, run and tests

Run commands from this repository root unless a `cd` is shown. Use a disposable checkout and fictional data for first setup. Dependencies, SDKs, signing material and personal data are not bundled. The following are continuation instructions grounded in the retained source, **not commands executed or newly certified by this handover**.

```powershell
python -m http.server 8765 --bind 127.0.0.1
```

/external-sources/StandaloneTools/mechanism-workbench.html

Selected project check:

No independent automated production test suite is included for this module/single-file package. Use the project-specific checks below and the shared host test suite where applicable; do not invent an `npm test` command.

For the documentation demo alone, serve this repository on loopback with `python -m http.server 8765 --bind 127.0.0.1` and open `/demo.html`. Choose a free port if another preview is running. JavaScript syntax can be checked with `node --check demo-source/runtime.js`. `python demo-source/rebuild.py` rewrites demo.html, so run it only in a disposable checkout or an authorised demo-editing session. A local server cannot provide missing HA/CAD/NAS functions. Inspect browser tests for installed dependencies, fixture requirements and network targets before running them with the approved browser tooling.

## Data, configuration and backup boundaries

Workspace/defaults live in browser storage; explicit export/import moves them between devices. Motion CSV alone may omit editable configuration. Included door dimensions are unconfirmed examples.

Defaults are browser-local. Export/import carries the workspace between devices. A CSV records motion results but does not necessarily preserve every editable setting.

Git preserves reviewed source and documentation. It does not copy browser storage, application databases, uploaded models/photos, accepted device settings, SDKs or credentials. Maintain independent recovery copies of the data identified above, including matching configuration and asset versions. Never add real secrets to examples, issues or logs. Private source copies on GitHub are not proof of a complete NAS/offsite data backup.

## Current verification and Git state

Before these documentation edits on 14 October 2026, this package was clean on branch `main` at `9ad96d9fc9cdddbc2e4ebdd897aa5a744a53f600` and its private upload was verified. All 1 manifest-listed source entries matched their stored checksums before editing. The upload follow-up has completed all 17 repositories and is paused; it does not run this tool or back up its live data.

These handover pages and README links accompany the private source package. Preserve them when continuing; stage only reviewed changes. Recheck current `git status --short --branch` and `git diff` before starting. No project-specific background schedule was inspected or changed in this documentation pass. Any service schedules in older notes are historical claims to verify in the actual deployment.

Earlier package checks and limits are recorded in [VALIDATION.md](../VALIDATION.md). This handover adds documentation/link/whitespace/secret and source-preservation checks only. No current NAS release, real hardware state, fresh installation, complete data restoration or offsite-backup freshness was verified here.

## Recovery approach

1. Preserve the current installation/data before changing it. Identify the exact code commit and data snapshot required; do not assume this package matches the running service.
2. Recover source into a new folder. Verify the source manifest and restore the project-specific configuration/assets described above separately. Recreate dependencies from the retained project files and guides.
3. Restore user data into an isolated instance or clean test browser. Check a representative editable record, associated files and save/reload behaviour, then compare to the original. Do not test recovery by overwriting production.
4. Record what actually restored and what remains missing. A demo opening or a passing syntax check is not a production recovery drill. Real deployment/device actions need the existing authorised workflow.

## Known limits and next work

The door preview uses sampled motion and conservative envelopes. It does not certify collisions or strength of a finished 3D assembly. The screenshot uses the included editable example, whose dimensions are explicitly unconfirmed.

**Priority:** Verify limiting positions and invalid-link geometry using known cases; reload an exported workspace before clearing browser data. Sampled envelopes do not prove full 3D clearance or structural strength.

Common symptoms to check for this tool:

- Impossible linkage: check link lengths, branch selection and closure through the whole range.
- Large pressure spike: inspect leverage and proximity to a dead centre.
- Saved defaults appear different: confirm the same browser/origin or import the intended export.

Keep [the release checklist](../RELEASE-CHECKLIST.md) and [third-party notes](../THIRD-PARTY.md) with the package. Original contributions use MIT; bundled/upstream code and assets keep their own licences. Public publication is a separate decision; preparing documentation is not permission to publish.
