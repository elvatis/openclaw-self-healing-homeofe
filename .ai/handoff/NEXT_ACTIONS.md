# NEXT_ACTIONS (AAHP)

## Status Summary

| Status  | Count |
|---------|-------|
| Done    | 9     |
| Ready   | 1     |
| Blocked | 1     |

---

## Ready - Work These Next

### T-010 [medium] - Expose self-heal status for external monitoring
- **Goal:** Let external tools (dashboards, CLI, other plugins) query self-heal state.
- **Context:** No way to know which models are in cooldown, how many heals occurred, or WhatsApp status without reading the raw state file. T-009 now emits structured events, but a queryable status endpoint is still needed.
- **What to do:**
  - Register a plugin command or API endpoint (e.g., `openclaw self-heal status`)
  - Return JSON with: cooldown models, WhatsApp status, cron heal history, last heal actions
  - Alternatively, write a status summary to a well-known file path
- **Files:** `index.ts`, `test/index.test.ts`
- **Definition of done:** External tools can query self-heal status; tests verify status output format.
- **GitHub Issue:** #4

---

## Blocked

### T-005 [high] - Implement structured plugin health monitoring and auto-disable
- **Blocked by:** Waiting for `openclaw plugins list --json` API from openclaw core
- **Goal:** Monitor plugin health and auto-disable failing plugins using structured JSON output.
- **Context:** Current code has a stub that parses plain text output from `openclaw plugins list`. No robust parsing is possible without the `--json` flag.
- **What to do (when unblocked):**
  - Parse `openclaw plugins list --json` output for plugin status
  - Auto-disable plugins with `status=error` (respecting `pluginDisableCooldownSec`)
  - Create GitHub issues for disabled plugins
- **Files:** `index.ts`, `test/index.test.ts`
- **Definition of done:** Failing plugins are detected via JSON API and auto-disabled; tests cover detection and disable logic.
- **GitHub Issue:** #3

---

## Recently Completed

| Task  | Title | Date |
|-------|-------|------|
| T-009 | Emit structured observability events for heal actions | 2026-02-28 |
| T-008 | Add dry-run mode for safe validation of healing logic | 2026-02-28 |
| T-007 | Add active model recovery probing to shorten cooldown periods | 2026-02-28 |
| T-006 | Support configuration hot-reload without gateway restart | 2026-02-28 |
| T-004 | Add TypeScript build pipeline and type-checking | 2026-02-27 |
