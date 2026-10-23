# Main documentation tasks

This list owns main documentation preparation. Product implementation tasks belong to `TASKS.md`. Complete these tasks in order, reusing valid existing artifacts and completion evidence when resuming.

## Completion and tracking

Each document task and its issue track development through first approval in the active pass. After that approval, mark the task complete. Ordinary later edits leave it complete and its issue closed. An explicit cursor reset reopens DOCS-002–009 and the same issues for the next pass; DOCS-001 and existing documents are retained. Selected mode preapproval may satisfy human checkpoints within its scope; it does not waive QC or publication. The user may preapprove future checkpoints at any time.

Include the checked task in `DOCS_TASKS.md` in the same commit that submits the approved document and records its first approval. If the reviewed document was already published unchanged, retain that exact document state in the acceptance commit; do not rewrite it merely to create a diff. Push and verify remote containment before closing the corresponding issue or advancing.

When tracking is enabled, each `DOCS-*` task maps to one issue in the `sdd-docs-main` milestone. Verify the milestone, all nine issues and their associations before modifying the repository. Reuse their stable identities on resume. Close issues only after the corresponding completion commit is published and verified. With tracking disabled, apply the same local task and checkpoint requirements.

The running SDD Manager package's `assets/DOCS_TRACKING_TEMPLATE.json` supplies the fixed milestone title/description and all nine issue definitions, including dependencies. Use those definitions through sdd-forge; this Markdown remains the local completion owner. Neither asset records provider handles or proves runtime eligibility. Resolve source/content conflicts before projection rather than replacing this list or inventing issue text.

## Mode and pass control

Record the selected doc-design mode, current pass/cursor, scope revision sequence when present and actual approval/delegation basis here as preparation proceeds. Interactive/onepass is the ordinary default. Autodoc keeps PROJECT approval active and preapproves later document checkpoints through TASKS; its DOCS-008 boundary stops before DOCS-009. For predefined autodoc scope sequences, autoloop is the default unless human-controlled multipass is requested: announce that later PROJECT approvals are waived after the first approval, make delegated new material decisions with visible rationale, and continue through only the defined passes. Human-controlled multipass retains each PROJECT approval and the reset/advance stop.

Use the coordinator's cursor-reset procedure: record the prior/next pass and scope, uncheck DOCS-002–009 and publish/read back the reset commit before reopening/readback of existing issues. Revise retained documents rather than recreate them. At an autodoc final DOCS-008 stop, retain DOCS-009 and the milestone open until the human explicitly advances. Do not infer complete preparation, Git integration or implementation from a completed pass.

## Preparation

- [x] DOCS-001 — Initialize the repository for SDD Manager.
    - Inspect root `AI_DISCLOSURE.md`, `SDD-MANAGER.md`, `AGENTS.md` and `SKILL_DISCOVERY_PROTOCOL.md` before copying. Preserve existing files and copy only missing files from the bundled templates.
    - Record which root files existed and which were copied; verify copied bytes and preserved content.
    - Establish/reconcile `docs/dev/HANDOFF.md` as generated checkpoint metadata, outside the four-file presence/copy test. Include it with this task's completion and initialization result, push and verify; then close and verify its issue when tracking is enabled.
    - Report initialization. If some but not all of the four root files existed initially, warn with the retained/copied filenames and end the turn before document work, unless the user explicitly preapproved continuation through this checkpoint. If none or all existed, continue without an additional approval pause.
- [ ] DOCS-002 — Prepare and accept PROJECT.
    - Establish the project brief: purpose, users, outcomes, scope, non-goals and consequential constraints; identify material assumptions and unresolved decisions.
    - Present the proposal and complete its selected human-approval or scoped-preapproval checkpoint.
- [ ] DOCS-003 — Prepare and accept ARCHITECTURE.
    - Define major system blocks, relationships, dependency direction and consequential structural decisions from the accepted brief.
    - Present the proposal and complete its selected human-approval or scoped-preapproval checkpoint.
- [ ] DOCS-004 — Prepare and accept DECOMPOSITION.
    - Define component responsibilities, collaboration, ownership and design-level interface boundaries consistently with ARCHITECTURE.
    - Present the proposal and complete its selected human-approval or scoped-preapproval checkpoint.
- [ ] DOCS-005 — Prepare and accept SPEC.
    - Specify observable behavior, interfaces, error contracts, required qualities and acceptance conditions from the accepted design.
    - Complete required SPEC QC and its selected approval/preapproval checkpoint.
- [ ] DOCS-006 — Prepare and accept PLAN.
    - Define delivery phases, milestones, dependencies and exit conditions against SPEC.
    - Complete PLAN QC, then satisfy its selected approval/preapproval checkpoint.
- [ ] DOCS-007 — Prepare and accept layout.
    - Allocate source, tests, documentation and artifacts to physical paths consistently with the accepted design and PLAN.
    - Review layout against the design and PLAN, update the PLAN review report, then satisfy its selected approval/preapproval checkpoint.
- [ ] DOCS-008 — Prepare and accept TASKS.
    - Derive executable tasks, dependencies and required milestone/phase review units from accepted SPEC, PLAN and layout.
    - Complete required task-list QC and its selected approval/preapproval checkpoint. Apply the mode's stop/reset/advance boundary after recording completion. Do not start implementation or project implementation-phase objects yet.
- [ ] DOCS-009 — Pass documentation package QC.
    - Require all preceding tasks complete and their issue closures verified when tracking is enabled.
    - Review the entire document set, necessary children and QC reports for consistency, traceability, delivery readiness and unresolved blockers. Check initialization, orientation, human acceptance and publication evidence.
    - Resolve blockers through their owning documents and recheck affected readiness and acceptance. Retain the package QC report with the preparation documents.
    - Refresh `docs/dev/HANDOFF.md` with the package outcome, evidence and next boundary, retaining later integration/milestone effects as requiring confirmation. Commit the handoff, passing report and this task marked complete together, push and verify; then close and verify the final QC issue.

## Integration and final checkpoint

After DOCS-009, explicitly merge the verified documentation branch into the actual default branch. Verify the merged result, commit, push and confirm remote containment. Then close and verify the `sdd-docs-main` milestone when tracking is enabled. Failed or uncertain integration or milestone closure remains pending; checked tasks alone do not complete preparation.

Report the package QC result, published merge and tracking status. Confirm the final checkpoint before implementation and obtain the authorized implementation range. Proceed without another pause only when explicit preapproval covers that checkpoint and implementation scope is already established.

On interruption, recover the earliest unmet operation from documents, acceptance decisions, Git and hosted evidence. Preserve a pending mixed-initialization decision. Do not regenerate the list, infer acceptance from file presence or repeat completed work. Honor explicit narrower scope, local-only or no-merge instructions and report any remaining completion steps.

## Active preparation record

- Mode: autodoc/autoloop, explicitly requested on 2026-10-23; reporting Standard after Explicit bootstrap.
- Current scope: pass 1, playable classic baseline. Cursor: DOCS-002, first PROJECT approval pending.
- Approval basis: first PROJECT approval remains active; later PROJECT approvals are waived, as announced before this proposal. Approval of the initial PROJECT and proposed cross-scope choices authorizes the predefined sequence and resets, with ARCHITECTURE through TASKS preapproved. No implementation is authorized.
- Stop: after DOCS-008 in pass 6, before DOCS-009, package QC, documentation integration or implementation activation.
- Tracking: enabled by root AGENTS.md; sdd-docs-main milestone 2 and DOCS-001–009 issues 10–18 verified before repository writes.
- Initialization: retained all four existing root files byte for byte; copied none. Preservation checked against pre-write SHA-256 observations. All-present initialization permits continuation without an additional pause.
- Credential continuity: reused the existing excluded, untracked gh.tkn; added the conventional *.tkn rule to root .gitignore after projection verification. No credential value enters Git.
- Publication: every owned commit must be pushed and read back before further work. Initialization issue closure follows publication.

### Authorized cumulative scope sequence

1. Classic falling-piece game: movement, rotation, gravity, clearing, score, game over and restart.
2. Add hold, ghost, 7-bag, SRS wall kicks, hard drop and full-gravity-interval lock delay including hard drop.
3. Add dynamic ghost visibility above the midline.
4. Add penetrator activation, four-line-clear bonus awards, capacity three, white rendering and bonus indicators; use the same deepest legal landing for hard drop and ghost.
5. Add six session-only settings and next preview.
6. Add independent URL > cookie > default resolution, cookie/URL updates on changes and saving explicit valid URL values including defaults.

Later scope remains here until adopted into each current project document. Keep document-preparation controls out of PROJECT, ARCHITECTURE, DECOMPOSITION, SPEC, PLAN, layout and TASKS.

### Proposed exploration decisions for initial approval

These are agent proposals, not claims of prior human agreement. The initial PROJECT approval is requested together with these choices; later material decisions within the sequence are delegated under autoloop.

- Platform: desktop keyboard browser game, TypeScript with Canvas board rendering and HTML controls; no backend, account, multiplayer or mobile touch requirement. Canvas keeps grid rendering direct; HTML makes settings and status accessible. A full UI framework adds no necessary capability for this scope.
- Board and baseline: 10 columns by 20 visible rows, seven tetrominoes, random independent selection, collision-checked rotation without kicks, soft drop, fixed gravity, immediate locking on failed downward movement, game over on blocked spawn, restart and pause. Precise controls/scoring remain downstream contract details.
- Ghost midline: show dynamically only when every occupied cell in the projected piece lies in rows 10–19 (zero-based); straddling projections remain hidden. Evaluate cells, not the bounding-box anchor.
- Delayed lock: start at first contact with a valid grounded position; lateral moves and rotation while grounded do not reset elapsed time. Leaving ground cancels it; new contact starts a fresh interval. Pause and hidden-page suspension freeze gameplay time. Hard drop follows this rule unless immediate locking is selected.
- Penetrator: activation is one-way for the current piece and spends a bonus immediately. It changes neither existing cells nor score. Hold stores tetromino type only; a swapped-in piece is normal, and a spent bonus is not refunded. Hold is limited to once per spawned piece. Restart clears bonuses and hold.
- Penetrator legality: pass through occupied cells only within board boundaries; scan all reachable vertical rows for the deepest fully non-overlapping position. Hard drop and ghost share this result. Prevent movement/rotation that leaves no reachable valid locking position; overlap never causes an invalid lock or a frozen lock-ready state. Collision with board edges remains enforced. Award bonuses after a simultaneous four-line clear, capped at three.
- Settings take effect immediately. Disabling hold preserves its stored type but prevents swaps. Disabling hard drop ignores its hotkey; preview/ghost controls affect display only. Switching to interval locking starts a fresh timer if grounded; switching to failed-down locking cancels that timer and waits for the next failed down attempt. Changing hard-drop policy is prospective, without retroactively locking a previous drop. Restart preserves settings.
- Defaults: dynamic ghost, hard drop enabled, preview enabled, hard drop follows general policy, full-interval general locking, hold enabled. Dynamic behavior is the default when its capability is adopted; earlier ghost scope uses always-visible behavior.
- Configuration parsing: validate each setting independently; an invalid URL value falls back to valid cookie then default and does not overwrite a valid cookie. Invalid cookie values fall back to default. Duplicate URL keys use the first occurrence. Accept canonical enumerated values only; do not coerce arbitrary text. Preserve unrelated query parameters and fragments. Use URL replacement without reload; catch cookie/URL-write failures so the selected in-memory setting still works.
- Persistence: use individual cookies with a one-year lifetime, Path=/ and SameSite=Lax, adding Secure on HTTPS. A valid explicit URL value is copied to its cookie even when it equals the default. Omission retains its cookie. No persistence is introduced until its scope is active.
- Browser coverage: Chromium primary, Playwright-managed Firefox secondary, headless; reference BROWSER_DEV_POLICY.md for provisioning/isolation and require fresh isolated provisioning evidence in setup tasks. No browser installation is necessary for document preparation.
- Versioning: first delivered playable phase v0.1.0; subsequent additive pre-1.0 phases advance the minor version, corrections the patch. Publish a corresponding tag, release and RELEASE-NOTES.md after each subsequently authorized implementation phase is verified and integrated. Documentation passes do not trigger product releases.

### Current evidence

DOCS-001: all four roots retained, zero copied; initialization result and checked task committed together. Push/readback and issue closure require external confirmation after this checkpoint commit.


DOCS-001 publication confirmed: 8e82c5325240056a77c91b6a94be4809e80a8d75 pushed to design-docs/main with exact remote readback. Issue 10 evidence comment, closed state, completed reason and milestone 2 association read back successfully.

DOCS-002 proposal: PROJECT and README prepared for initial human approval. The brief covers the classic baseline only, with fixed gravity, independent random selection, collision-checked rotation and failed-down locking. Pause is a proposed usability detail. TypeScript/Canvas/HTML and the two-browser test targets are proposed constraints. No downstream document has been authored. The first PROJECT approval is requested together with the exploration decisions above; DOCS-002 remains unchecked and issue 11 remains open.

Proposal QC: reviewed against the supplied baseline and root instructions; purpose, users, principal scope, constraints and non-goals are coherent. Confirmed no preparation-mode/pass/reset narrative or later enhancement requirements appear in PROJECT. Checked relative links, Markdown heading/list spacing and git diff --check. No browser execution is needed for this document-only proposal. Refined the initial baseline proposal to fixed gravity to keep its scope minimal; level progression is not required.
