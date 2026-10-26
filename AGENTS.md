# Agent instructions — default

## Repository-specific deterministic quality contract (2026-10-26)

**Project:** Home Assistant community repository containing AppDaemon scripts, templates and automation modules.

**Engineering requirements:** Validate new Python, YAML, Jinja and integration config independently; don't assume all scripts run outside Home Assistant.

**Verification commands:** python -m compileall -q python_script appdaemon; validate changed yaml in HA runtime.

Before completion, run relevant checks and report exact pass/fail results. Add regression tests for changed behavior, bounds and failure paths. Never weaken/delete/skip tests, suppress warnings, or change CI thresholds to fabricate green results. Changes to `QUALITY_GATES.md`, this contract, and workflows require human review. The `quality` status must be required in branch protection to make the gate enforceable. If native dependencies prevent a test, explicitly report the blocker rather than claiming success. Existing project instructions have precedence for build setup; this section augments them.
