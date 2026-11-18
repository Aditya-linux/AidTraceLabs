# Privacy Cleanup Report

Generated: 2026-11-18

---

## Step 1 — Backup file counts

| Location | `docs/issues-draft/` file count |
|---|---|
| Working tree (`AidTraceLabs/docs/issues-draft/`) | 137 |
| Backup destination (`aidtrace-private/docs/issues-draft/`) | 137 |

**Counts match.** Backup destination: `c:\Users\Hp\OneDrive\Documents\aidtrace-private\`

Files backed up:
- `docs/drips-application-notes.md`
- `docs/backlog-audit.md`
- `docs/manual-test-checklist.md`
- `docs/issues-draft/` (entire directory, 137 files including all subdirectories)
- `.env.local` — copied to backup folder only, NOT committed to any repo
- `.env.demo` — copied to backup folder only, NOT committed to any repo

---

## Step 2 — Open PR check for the three fix branches

Command: `gh pr list --repo AidTraceHQ/AidTraceLabs --state open --json number,title,headRefName`

| Branch | Open PR |
|---|---|
| `fix/final-readiness` | None |
| `fix/readme-screenshots` | None |
| `fix/wave-guidelines` | None |

(PR #40 `docs/backlog-audit` was open and was closed in Step 6.)

---

## Step 3 — Remove `docs/drips-application-notes.md` from origin/main

| Field | Value |
|---|---|
| Branch | `main` |
| Commit hash | `b10bdae` |
| Message | `chore: remove internal Drips application notes` |
| Files changed | `docs/drips-application-notes.md` (deleted, 77 lines) |
| Pushed to | `origin/main` |

---

## Step 4 — Remove `docs/manual-test-checklist.md` from origin/main

| Field | Value |
|---|---|
| Branch | `main` |
| Commit hash | `f0f69d2` |
| Message | `chore: remove internal manual test checklist` |
| Files changed | `docs/manual-test-checklist.md` (deleted, 98 lines) |
| Pushed to | `origin/main` |

---

## Step 5 — Remove `docs/drips-application-notes.md` from three fix branches

### fix/final-readiness

| Field | Value |
|---|---|
| Branch | `fix/final-readiness` |
| Commit hash | `49a4af9` |
| Message | `chore: remove internal Drips application notes` |
| Files changed | `docs/drips-application-notes.md` (deleted) |
| Pushed to | `origin/fix/final-readiness` |

### fix/readme-screenshots

| Field | Value |
|---|---|
| Branch | `fix/readme-screenshots` |
| Commit hash | `f032365` |
| Message | `chore: remove internal Drips application notes` |
| Files changed | `docs/drips-application-notes.md` (deleted, 77 lines) |
| Pushed to | `origin/fix/readme-screenshots` |

### fix/wave-guidelines

| Field | Value |
|---|---|
| Branch | `fix/wave-guidelines` |
| Commit hash | `7d9d0cf` |
| Message | `chore: remove internal Drips application notes` |
| Files changed | `docs/drips-application-notes.md` (deleted) |
| Pushed to | `origin/fix/wave-guidelines` |

---

## Step 6 — Close PR #40 and delete remote branch

**PR #40 close:**
```
✓ Closed pull request AidTraceHQ/AidTraceLabs#40 (docs: audit one-week contributor backlog)
```

**Remote branch deletion:**
```
To https://github.com/AidTraceHQ/AidTraceLabs.git
 - [deleted]         docs/backlog-audit
```

Local branch `docs/backlog-audit` was NOT deleted (as instructed).

---

## Step 7 — Add vercel-out.txt to .gitignore

`vercel-out.txt` was not present in `.gitignore`. It was appended on a new line.

| Field | Value |
|---|---|
| Branch | `main` |
| Commit hash | `e06e772` |
| Message | `chore: gitignore vercel-out.txt` |
| Files changed | `.gitignore` (1 line added) |
| Pushed to | `origin/main` |

---

## Step 8 — Private GitHub repo created and backup pushed

**Repo URL:** https://github.com/AidTraceHQ/AidTraceLabs-private

**Commit:** `0691d13` — `initial: private planning files backup` — 141 files

**`.gitignore` in private repo:**
```
.env*
*.env
.env.local
.env.demo
```

**`.env.local` and `.env.demo` staged check:** Neither file appeared in `git status` before commit — both were excluded by `.gitignore`.

**Full `git ls-files` output from private repo (no `.env` files present):**

```
.gitignore
docs/backlog-audit.md
docs/drips-application-notes.md
docs/issues-draft/01-local-calendar-date.md
docs/issues-draft/02-persist-theme-choice.md
docs/issues-draft/027-retry-safe-record-create.md
docs/issues-draft/028-preserve-primary-transaction-error.md
docs/issues-draft/029-bound-graceful-shutdown.md
docs/issues-draft/03-fix-toast-timer-race.md
docs/issues-draft/030-retry-safe-read-routes.md
docs/issues-draft/031-reject-reused-runtime-secrets.md
docs/issues-draft/032-validate-canonical-cors-origins.md
docs/issues-draft/033-horizon-failure-contract-tests.md
docs/issues-draft/034-enforce-record-invariants-in-database.md
docs/issues-draft/035-check-applied-migration-checksums.md
docs/issues-draft/036-sync-record-form-network-default.md
docs/issues-draft/037-separate-activity-search-state.md
docs/issues-draft/038-lock-record-form-during-save.md
docs/issues-draft/039-reject-reversed-date-filters.md
docs/issues-draft/04-refresh-active-wallet-role.md
docs/issues-draft/040-timeout-browser-api-requests.md
docs/issues-draft/041-compute-ledger-aggregates-once.md
docs/issues-draft/042-page-horizon-wallet-activity.md
docs/issues-draft/043-add-api-contract-examples.md
docs/issues-draft/044-stabilize-serverless-import-test.md
docs/issues-draft/045-test-node-22-in-ci.md
docs/issues-draft/046-route-admin-role-mutations-through-transaction-helper.md
docs/issues-draft/047-handle-unhandled-rejections-and-uncaught-exceptions.md
docs/issues-draft/048-configure-http-server-timeouts.md
docs/issues-draft/049-broaden-transient-database-error-classification.md
docs/issues-draft/05-edit-organization-display-name.md
docs/issues-draft/050-map-body-parser-errors-to-4xx.md
docs/issues-draft/051-bound-verification-request-duration.md
docs/issues-draft/052-add-timeouts-to-migration-pool.md
docs/issues-draft/053-bound-idle-in-transaction-database-time.md
docs/issues-draft/054-abort-server-work-on-client-disconnect.md
docs/issues-draft/055-centralize-database-error-mapping.md
docs/issues-draft/056-bound-database-client-checkout-wait.md
docs/issues-draft/057-handle-idle-pool-client-errors.md
docs/issues-draft/058-reject-example-session-secret.md
docs/issues-draft/059-test-csrf-enforcement-on-mutations.md
docs/issues-draft/06-beneficiary-record-filters.md
docs/issues-draft/060-test-forged-wallet-signatures.md
docs/issues-draft/061-test-expired-session-rejection.md
docs/issues-draft/062-test-logout-everywhere-sessions.md
docs/issues-draft/063-test-database-backed-rate-limits.md
docs/issues-draft/064-test-record-input-validation.md
docs/issues-draft/065-test-filter-injection-and-sanitization.md
docs/issues-draft/066-test-request-body-limits.md
docs/issues-draft/067-test-audit-coverage-for-mutations.md
docs/issues-draft/068-test-authorization-route-matrix.md
docs/issues-draft/069-test-pagination-cursor-integrity.md
docs/issues-draft/07-traceable-role-change-audit.md
docs/issues-draft/070-cache-negative-verification-outcomes.md
docs/issues-draft/071-support-muxed-account-recipients.md
docs/issues-draft/072-bound-horizon-verification-retries-and-deadline.md
docs/issues-draft/073-capture-transaction-memo.md
docs/issues-draft/074-assert-mainnet-horizon-and-explorer-selection.md
docs/issues-draft/075-align-operation-amount-parsing.md
docs/issues-draft/076-bound-horizon-response-size.md
docs/issues-draft/077-index-admin-roles-order.md
docs/issues-draft/078-validate-migration-filenames.md
docs/issues-draft/079-populate-audit-metadata.md
docs/issues-draft/08-database-readiness-endpoint.md
docs/issues-draft/080-record-session-last-seen.md
docs/issues-draft/081-align-record-pagination-index.md
docs/issues-draft/082-schema-drift-test.md
docs/issues-draft/083-clamp-ledger-page-after-reload.md
docs/issues-draft/084-add-activity-empty-and-error-states.md
docs/issues-draft/085-warn-before-discarding-record-form.md
docs/issues-draft/086-add-retry-to-ledger-error.md
docs/issues-draft/087-revalidate-network-switch-while-connected.md
docs/issues-draft/088-refresh-single-record-without-refetch.md
docs/issues-draft/089-return-ledger-total-count.md
docs/issues-draft/09-audit-security-rejections.md
docs/issues-draft/090-format-record-amounts-consistently.md
docs/issues-draft/091-coalesce-ledger-reloads-after-mutation.md
docs/issues-draft/092-sort-ledger-on-the-server.md
docs/issues-draft/093-guard-csv-export-against-formula-injection.md
docs/issues-draft/095-export-audit-log-as-csv.md
docs/issues-draft/096-add-verification-columns-to-csv-export.md
docs/issues-draft/097-export-beneficiary-records-as-csv.md
docs/issues-draft/098-document-api-error-contract.md
docs/issues-draft/099-document-cursor-pagination-contract.md
docs/issues-draft/10-clean-expired-ephemeral-rows.md
docs/issues-draft/100-pin-and-verify-node-runtime.md
docs/issues-draft/101-log-request-duration-and-status.md
docs/issues-draft/102-log-startup-configuration-summary.md
docs/issues-draft/103-trap-focus-in-record-and-disbursement-dialogs.md
docs/issues-draft/104-add-table-semantics-and-keyboard-scroll.md
docs/issues-draft/105-associate-record-form-errors-with-fields.md
docs/issues-draft/108-announce-stream-and-verification-status.md
docs/issues-draft/109-enlarge-touch-targets-for-compact-controls.md
docs/issues-draft/11-protect-last-admin.md
docs/issues-draft/111-add-favicon-and-color-scheme.md
docs/issues-draft/112-add-skip-to-content-link.md
docs/issues-draft/113-cancel-superseded-ci-runs.md
docs/issues-draft/114-align-compose-and-env-bootstrap.md
docs/issues-draft/115-measure-and-enforce-test-coverage.md
docs/issues-draft/116-cache-hashed-static-assets.md
docs/issues-draft/117-align-rate-limit-error-payload.md
docs/issues-draft/118-adopt-type-aware-eslint.md
docs/issues-draft/119-add-app-error-boundary.md
docs/issues-draft/12-shared-per-ip-rate-limits.md
docs/issues-draft/120-version-column-for-record-concurrency.md
docs/issues-draft/121-cap-active-sessions-per-wallet.md
docs/issues-draft/122-add-migration-status-and-dry-run.md
docs/issues-draft/13-separate-runtime-and-migration-db-roles.md
docs/issues-draft/14-verify-postgres-ingress-controls.md
docs/issues-draft/15-guard-admin-seed-target.md
docs/issues-draft/16-serialize-migration-runs.md
docs/issues-draft/17-security-response-headers.md
docs/issues-draft/18-configure-browser-horizon-endpoints.md
docs/issues-draft/19-bound-activity-request-lifecycle.md
docs/issues-draft/20-bookmark-ledger-filters.md
docs/issues-draft/21-remote-deployment-smoke-check.md
docs/issues-draft/22-correlated-safe-api-logs.md
docs/issues-draft/23-show-verification-check-time.md
docs/issues-draft/24-enforce-append-only-audit.md
docs/issues-draft/25-tested-backup-restore-runbook.md
docs/issues-draft/26-reconcile-deployment-status-docs.md
docs/issues-draft/_created.md
docs/issues-draft/_dropped/094-add-utf8-bom-to-csv-export.md
docs/issues-draft/_dropped/106-respect-reduced-motion-for-animations.md
docs/issues-draft/_dropped/107-raise-muted-text-contrast.md
docs/issues-draft/_dropped/110-indicate-active-section-tab.md
docs/issues-draft/_guidelines-block.md
docs/issues-draft/_index.md
docs/issues-draft/_overlap-report.md
docs/issues-draft/_trivial-review.md
docs/issues-draft/existing/13-public-verification-page.md
docs/issues-draft/existing/16-dashboard-totals.md
docs/issues-draft/existing/18-scheduled-re-verification.md
docs/issues-draft/existing/19-beneficiary-wallet-acknowledgment.md
docs/issues-draft/existing/existing/20-webhook-or-email-alerts.md
docs/issues-draft/existing/21-playwright-end-to-end-tests.md
docs/issues-draft/existing/24-internationalization-groundwork.md
docs/issues-draft/existing/28-design-reentering-a-voided-payment.md
docs/issues-draft/existing/_catalog.md
docs/issues-draft/existing/ready-additions.md
docs/manual-test-checklist.md
```

**Confirmed: no `.env.local` or `.env.demo` in tracked files.**

---

## Step 9 — docs/issues-draft/existing/ comparison with filed GitHub issues

The `existing/` directory contains rewritten drafts of 8 GitHub issues that the `_catalog.md` identified as "Needs rewriting," plus two planning files (`_catalog.md`, `ready-additions.md`).

### Notes on `_catalog.md` and `ready-additions.md`

- **`_catalog.md`**: A full audit of all 18 issues (#11–#28). Read-only inventory, not a rewrite of a specific issue.
- **`ready-additions.md`**: Contains `## Out of scope` and `## Depends on` sections ready to append to the 7 "Wave-ready" issues (#11, #12, #14, #15, #17, #22, #23), which currently lack those two sections on GitHub. No issue number maps 1:1 to this file.

### Comparison table

| File | Matched GitHub issue # | Title match | Content differs? | Notes |
|---|---|---|---|---|
| `13-public-verification-page.md` | #13 | ✓ Exact | Yes — draft is expanded | Draft has detailed `## Context` with line references, explicit field-by-field consent rules, and fuller test expectations. GitHub body (3942 chars) already has all 7 sections — it appears the draft was previously pushed. Minor wording differences remain. |
| `16-dashboard-totals.md` | #16 | ✓ Exact | Yes — significant | GitHub body (715 chars) is missing `## Out of scope` and `## Depends on`. Draft (2359 chars) adds both sections plus a detailed `## Context` with specific line references (`transparencyHandler`, `ledgerTotals`, etc.) and a note that the issue may be a candidate for closing/narrowing since most of #16 has already shipped. |
| `18-scheduled-re-verification.md` | #18 | ✓ Exact | Yes — expanded | GitHub body (3147 chars) has all sections. Draft (2866 chars) is similar in length; both have all 7 sections. Draft `## Context` cites specific line numbers and adds a "Decision required first" note. Minor substantive differences in acceptance criteria wording. |
| `19-beneficiary-wallet-acknowledgment.md` | #19 | ✓ Exact | Yes — expanded | GitHub body (2920 chars), draft (2633 chars). Both have all 7 sections. Draft has more explicit public-projection wording and an explicit field list under acceptance criteria. |
| `20-webhook-or-email-alerts.md` | #20 | ✓ Exact | Yes — expanded | GitHub body (2720 chars), draft (2442 chars). Both have all sections. Draft adds explicit SSRF, timeout, and secrets-logging requirements in acceptance criteria. |
| `21-playwright-end-to-end-tests.md` | #21 | ✓ Exact | Yes — expanded | GitHub body (2973 chars), draft (2692 chars). Both complete. Draft cites `src/freighter.ts`, `.github/workflows/ci.yml` specifically and adds an explicit Freighter-wrapper dependency note under `## Depends on`. |
| `24-internationalization-groundwork.md` | #24 | ✓ Exact | Yes — expanded | GitHub body (2557 chars), draft (2279 chars). Both complete. Draft adds line references for `toLocaleString()` calls and `formatAmount`, and an explicit note that addresses and status identifiers must not be auto-translated. |
| `28-design-reentering-a-voided-payment.md` | #28 | ✓ Exact | Yes — expanded | GitHub body (4878 chars), draft (4585 chars). Both complete. Draft has the same three options (A/B/C) and all acceptance criteria sections. Minor formatting differences. |
| `ready-additions.md` | #11, #12, #14, #15, #17, #22, #23 | Covers 7 issues | Yes — additive | Contains `## Out of scope` and `## Depends on` sections for the 7 Wave-ready issues. GitHub versions of these issues are missing both sections. This file has not been pushed to GitHub. |
| `_catalog.md` | All 18 issues (#11–#28) | Full audit | Informational | No single GitHub issue match. This is a planning/audit document. Not to be filed as an issue. |

### Summary

All 8 numbered draft files match their corresponding GitHub issues by filename and title. Every draft contains more detail than the current GitHub body — either an expanded `## Context` with specific source code line references, additional acceptance criteria, or sections missing from GitHub. The most significant gap is **#16**: the GitHub body is missing `## Out of scope` and `## Depends on`, and the draft notes that the issue may be closeable. No files have been deleted.

---

## Step 10 — Final verification

**`git ls-files docs/drips-application-notes.md docs/manual-test-checklist.md` on main:**
```
(empty — both files removed)
```

**`git log --all --oneline -- docs/drips-application-notes.md docs/manual-test-checklist.md`:**
```
7d9d0cf (origin/fix/wave-guidelines, fix/wave-guidelines) chore: remove internal Drips application notes
f032365 (origin/fix/readme-screenshots, fix/readme-screenshots) chore: remove internal Drips application notes
49a4af9 (origin/fix/final-readiness, fix/final-readiness) chore: remove internal Drips application notes
f0f69d2 chore: remove internal manual test checklist
b10bdae chore: remove internal Drips application notes
ed8c81e docs: finalize live demo readiness
70ad663 fix(security): isolate beneficiary pseudonym key
30f7b5d Agent host session 334a5039-1e9e-43e2-8fa0-516891570c26 - turn 1
9117a96 Fix verified ledger totals and privacy tests
927dde0 Agent host session 334a5039-1e9e-43e2-8fa0-516891570c26 - baseline checkpoint
e95ed2a Agent host session 445afcba-9aa6-479c-98a2-c5236ee09342 - turn 5
dfb18c8 docs: record Neon parity evidence and manual checks
```

Both removal commits (`b10bdae`, `f0f69d2`) are in history. Files are not tracked on main.

---

## Failures, skips, and notes

| Item | Status | Notes |
|---|---|---|
| Backup counts | ✓ 137/137 match | |
| `docs/drips-application-notes.md` removed from main | ✓ commit `b10bdae` | |
| `docs/manual-test-checklist.md` removed from main | ✓ commit `f0f69d2` | |
| `docs/drips-application-notes.md` removed from `fix/final-readiness` | ✓ commit `49a4af9` | |
| `docs/drips-application-notes.md` removed from `fix/readme-screenshots` | ✓ commit `f032365` | |
| `docs/drips-application-notes.md` removed from `fix/wave-guidelines` | ✓ commit `7d9d0cf` | |
| PR #40 closed | ✓ closed without comment | |
| `origin/docs/backlog-audit` deleted | ✓ deleted | |
| Local `docs/backlog-audit` branch | ✓ NOT deleted (as instructed) | |
| `vercel-out.txt` added to `.gitignore` | ✓ commit `e06e772` | |
| Private GitHub repo created | ✓ https://github.com/AidTraceHQ/AidTraceLabs-private | |
| `.env.local` / `.env.demo` excluded from private repo | ✓ confirmed by `git ls-files` | |
| `docs/issues-draft/existing/` comparison table | ✓ completed above | For review only — no files deleted |
