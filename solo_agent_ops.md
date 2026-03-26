# SOLO AGENT OPS
## A Strategic Card Game for Autonomous AI Agent Mastery

---

## GAME OVERVIEW

**Solo Agent Ops** is a solo card-based game that trains you to think like an expert autonomous AI agent. You'll practice the four critical pillars of agent work: Decision Trees, Phase Gates, Validators, and Session Continuity.

Each mission presents a real-world technical scenario. You must classify the task, choose the right workflow, verify prerequisites, execute properly, validate your work, and document the handoff—all while managing scope and maintaining continuity.

**Target Audience:** AI agents, automation engineers, technical leads
**Game Duration:** 5-20 minutes per mission
**Skill Level Progression:** Easy (Difficulty 1) → Expert (Difficulty 4)

---

## HOW TO PLAY

### Game Flow (One Round = One Mission)

1. **MISSION** — Read the scenario and technical context
2. **CLASSIFICATION** — Choose: small, medium, large, or complex
3. **PATH CHOICE** — Pick your workflow: quick mode, spec brief, or full pipeline
4. **GATE CHECK** — List the phase gates you must verify before proceeding
5. **EXECUTION SUMMARY** — Describe the actions you'd take
6. **VALIDATOR CHECK** — Prove your work passes all acceptance rules
7. **SESSION CONTINUITY** — Write a brief STATE.md-style handoff

---

## THE FOUR PILLARS EXPLAINED

### 🌳 Decision Trees
**Definition:** Classifying task complexity and selecting the right workflow path.

- **Small (Quick Mode):** 1-2 files, obvious fix, no scope risk
- **Medium (Spec Brief):** 3-5 files, defined scope, standard validation
- **Large (Full Pipeline):** 6+ files, multiple components, needs approval gates
- **Complex (Expert Route):** Ambiguous requirements, architectural risk, multi-session work

### 🚪 Phase Gates
**Definition:** Verification checkpoints that must be cleared before advancing.

Common gates:
- Branch strategy exists (naming convention respected)
- Ticket is linked and has acceptance criteria
- Design/spec is approved if architectural
- No blocking dependencies
- Scope is explicitly bounded
- Testing strategy is defined
- Reviewer is identified

### ✅ Validators
**Definition:** Objective rules proving your work meets quality standards.

Include:
- Branch naming convention
- Commit message format (type: scope - message)
- No scope creep (no untracked changes)
- All acceptance criteria met
- Code quality checks pass
- Documentation updated
- Tests present and passing

### 📝 Session Continuity
**Definition:** Handoff documentation ensuring the next agent can resume seamlessly.

Must contain:
- Current status (what was done)
- Next steps (what remains)
- Blockers (what's stuck)
- Decisions made (why we chose this path)
- Context (relevant links, approvals, design docs)
- Code locations (branches, commits, PRs)

---

## ROUND TEMPLATE

Copy and fill this template for each mission:

```
MISSION #: [Number]
TITLE: [Name]
DIFFICULTY: [1-4]
PRIMARY PILLAR: [Decision Trees / Phase Gates / Validators / Session Continuity]

---

YOUR RESPONSE:

Classification: [small / medium / large / complex]
Reasoning: [1-2 sentences]

Workflow Path Chosen: [quick mode / spec brief / full pipeline]
Reasoning: [Why this path?]

Phase Gates to Verify:
- [ ] Gate 1
- [ ] Gate 2
- [ ] Gate 3

Execution Summary:
[Describe the actions you'd take in 3-5 sentences]

Validator Check:
[How will you prove this passes all rules?]

Session Continuity Handoff:
[Write a mini STATE.md with status, next steps, blockers, decisions]

---

SCORE THIS ROUND:
[ ] +2 Correct classification
[ ] +2 Right workflow choice
[ ] +2 Respecting phase gates
[ ] +2 Avoiding scope creep
[ ] +2 Passing validators
[ ] +2 Clear handoff
[ ] -2 Over/under-engineering
[ ] -3 Skipping critical gates
[ ] -3 Untracked scope expansion
[ ] -3 Poor continuity

ROUND SCORE: _____ / 12
```

---

## SCORING SYSTEM

### Points Awarded
- **+2** Correct complexity classification
- **+2** Right workflow choice for that classification
- **+2** Identifying and respecting all phase gates
- **+2** Avoiding scope creep (no unnecessary additions)
- **+2** Passing all validator checks
- **+2** Clear, complete session continuity documentation

### Points Deducted
- **-2** Over-engineering (choosing full pipeline for small task) or under-engineering (quick mode for complex task)
- **-3** Skipping or failing to verify critical phase gates
- **-3** Untracked scope expansion or hidden changes
- **-3** Poor or missing session continuity documentation

### Scoring Scale
- **12 points** — Expert agent (mastered this mission type)
- **10-11 points** — Strong execution (minor refinements)
- **8-9 points** — Acceptable (met core objectives)
- **6-7 points** — Needs work (missed key gates or validators)
- **<6 points** — Study the ideal response (revisit this difficulty level)

### Campaign Tracking
Keep a running total across all 20 missions. Aim for 200+ total points to demonstrate mastery.

---

## PROGRESSION LEVELS

### Level 1: Fundamentals (Missions 1-5)
**Focus:** Master Decision Trees and basic validators
**Scenario Type:** Simple bugs, straightforward fixes
**Complexity:** Mostly "small" tasks; some "medium"
**Key Learning:** Recognize when quick mode is appropriate

### Level 2: Specification Work (Missions 6-10)
**Focus:** Phase Gates and workflow selection
**Scenario Type:** Small features, gate validation
**Complexity:** Mix of "small" and "medium"; some "large"
**Key Learning:** Verify prerequisites before building

### Level 3: Scope Management (Missions 11-15)
**Focus:** Avoiding scope creep and session continuity
**Scenario Type:** Ambiguous requests, multi-step tasks
**Complexity:** Mostly "large" and "complex"
**Key Learning:** Say no to unplanned work; document decisions

### Level 4: Expert Mastery (Missions 16-20)
**Focus:** All four pillars under pressure
**Scenario Type:** Complex ambiguity, multi-component, recovery
**Complexity:** All "complex"; multi-session scenarios
**Key Learning:** Integrate all pillars; handle recovery gracefully

---

## MISSIONS

---

## LEVEL 1: FUNDAMENTALS (Missions 1-5)

### 🎯 MISSION 1: The Obvious Typo

**Difficulty:** 1
**Primary Pillar:** Decision Trees

**SCENARIO:**
A user reports that the login form is displaying "Pasword" instead of "Password" in a label. The file is `src/components/LoginForm.jsx`. It's a one-line fix in a single, stable component. No other changes needed.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Small — Single file, obvious fix, zero scope risk |
| **Workflow Path** | Quick mode — No spec needed, no gates required |
| **Gates** | None required for quick mode |
| **Execution** | Fix typo in label, verify component renders, commit with message: "fix: correct spelling in LoginForm label" |
| **Validator Check** | Commit message matches format, file touched is only the component, no console warnings |
| **Handoff** | Status: Typo fixed and committed. Next: Merge to main. Blockers: None. Decisions: Used quick mode (no gates) because scope is trivial. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "small"
- **+2** Workflow: Selected quick mode (no unnecessary gates)
- **+2** Gates: Recognized no gates needed
- **+2** Scope: Made only the one-line change
- **+2** Validators: Commit message clean; one file only
- **+2** Handoff: Clear status and next action
- **-2** if you chose "medium" or added extra validation
- **-3** if you skipped commit message format

**Max Score:** 12

---

### 🎯 MISSION 2: Console Warning in Prod

**Difficulty:** 1
**Primary Pillar:** Validators

**SCENARIO:**
Your monitoring tool alerts that `src/utils/dataFormatter.js` is logging a deprecation warning to console in production. The warning says a function call is deprecated. You need to replace it with the modern API. The fix is localized and low-risk.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Small — Single utility file, one function update, no component changes |
| **Workflow Path** | Quick mode — Self-contained fix |
| **Gates** | None — scope is too small to require gates |
| **Execution** | Identify deprecated function, replace with modern API equivalent, run unit tests on dataFormatter to confirm it still works |
| **Validator Check** | Old function removed entirely, new function used, unit tests pass, console warning gone in test output, commit message: "fix: replace deprecated API in dataFormatter" |
| **Handoff** | Status: Deprecated API replaced; tests passing. Next: Code review and merge. Blockers: None. Decisions: Quick mode justified by single-file scope. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "small"
- **+2** Workflow: Quick mode justified and executed
- **+2** Gates: Correctly assumed no gates needed
- **+2** Scope: Only modified the one function, no extras
- **+2** Validators: Tests run; old API confirmed removed
- **+2** Handoff: Clear status and merge readiness
- **-2** if you over-tested (added new tests beyond what was needed)
- **-3** if you failed to run validators before handoff

**Max Score:** 12

---

### 🎯 MISSION 3: Dependency Version Bump

**Difficulty:** 1
**Primary Pillar:** Validators

**SCENARIO:**
A security advisory requests that you update `lodash` from 4.17.19 to 4.17.21 in `package.json`. The change is in one file. Your team's CI already runs all tests automatically. No logic changes needed.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Small — Single-file change, no code logic changes |
| **Workflow Path** | Quick mode — Dependency updates are low-risk maintenance |
| **Gates** | None required |
| **Execution** | Update version in package.json, let CI run its test suite automatically, monitor test results |
| **Validator Check** | Version updated in lock file, all CI tests pass, no vulnerabilities in audit output, commit message: "deps: update lodash to 4.17.21" |
| **Handoff** | Status: Dependency updated and CI tests passing. Next: Merge to main. Blockers: None. Decisions: Quick mode because it's a single-file, automated-verification change. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "small"
- **+2** Workflow: Quick mode appropriate for dependency updates
- **+2** Gates: Correctly assumed CI gates are automatic
- **+2** Scope: Only modified version; no refactoring
- **+2** Validators: CI results confirmed green
- **+2** Handoff: Status clear; ready for merge
- **-2** if you added manual testing beyond CI
- **-3** if you skipped waiting for CI validators

**Max Score:** 12

---

### 🎯 MISSION 4: Fix Button Color in Dark Mode

**Difficulty:** 1
**Primary Pillar:** Decision Trees

**SCENARIO:**
A design review flagged that the primary button color is too dark in dark mode and fails WCAG AA contrast requirements. The fix is in `src/styles/darkMode.css`, changing one color variable. No component changes; no logic affected.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Small — One CSS variable change, purely styling, no logic |
| **Workflow Path** | Quick mode — Single file, obvious fix path |
| **Gates** | None required for styling-only changes |
| **Execution** | Update the dark mode button color variable to a lighter shade, verify visually in both light and dark modes, run contrast checker tool to confirm WCAG AA compliance |
| **Validator Check** | Color variable updated, contrast checker confirms ≥4.5:1 ratio, no JavaScript changes, styling renders correctly on sample components |
| **Handoff** | Status: Button contrast fixed in dark mode CSS. Next: QA visual check. Blockers: None. Decisions: Quick mode; pure styling change with no scope risk. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "small"
- **+2** Workflow: Quick mode; no unnecessary process
- **+2** Gates: Recognized styling doesn't require approval gates
- **+2** Scope: Only the one color variable touched
- **+2** Validators: Contrast checker used; compliance verified
- **+2** Handoff: Clear status and next step
- **-2** if you added browser testing across 10 browsers
- **-3** if you changed the button component itself

**Max Score:** 12

---

### 🎯 MISSION 5: Add Missing Alt Text to Hero Image

**Difficulty:** 1
**Primary Pillar:** Validators

**SCENARIO:**
An accessibility audit found that the hero image in `src/components/HeroSection.jsx` is missing an `alt` attribute. This is a quick accessibility fix. The image displays the company logo; alt text should be "Company logo" or similar.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Small — Single component, one line fix (alt attribute) |
| **Workflow Path** | Quick mode — Accessibility fix, low risk |
| **Gates** | None required |
| **Execution** | Add appropriate alt attribute to img element: `alt="Company logo"`, test with accessibility inspector to confirm ARIA is correct, verify no console warnings |
| **Validator Check** | Alt text present and descriptive, accessibility inspector shows no errors, commit message: "a11y: add alt text to hero image", no other changes |
| **Handoff** | Status: Alt text added to HeroSection. Next: Merge after code review. Blockers: None. Decisions: Quick mode; single accessibility fix. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "small"
- **+2** Workflow: Quick mode appropriate
- **+2** Gates: No gates needed for accessibility fixes
- **+2** Scope: Only the alt attribute added
- **+2** Validators: Accessibility inspector confirms clean
- **+2** Handoff: Clear status and next step
- **-2** if you refactored the entire component
- **-3** if you failed to verify with an accessibility tool

**Max Score:** 12

---

---

## LEVEL 2: SPECIFICATION WORK (Missions 6-10)

### 🎯 MISSION 6: Add a Settings Panel

**Difficulty:** 2
**Primary Pillar:** Phase Gates

**SCENARIO:**
A ticket requests a new user settings panel. The ticket specifies: dark mode toggle, notification preferences (email, SMS), and language selector. You need to add this UI to `src/components/SettingsPanel/` (a new folder). The design is approved. The ticket is linked to an epic.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Medium — New component, 3 files (SettingsPanel.jsx, SettingsPanel.css, SettingsPanel.test.js), defined scope |
| **Workflow Path** | Spec Brief — Design approved, scope is clear, no architectural risk |
| **Gates to Verify** | ✓ Ticket linked (yes, epic reference provided) ✓ Design approved (stated) ✓ Acceptance criteria clear (3 toggles specified) ✓ No blocking dependencies ✓ Test strategy defined (unit tests on toggle logic) |
| **Execution** | Create SettingsPanel folder with component, styles, and tests. Implement three toggles with state management (React hooks). Add to navigation. Pass all unit tests. |
| **Validator Check** | All three toggles functional; state persists (localStorage or backend call); tests cover toggle logic; CSS passes linter; commit message: "feat: add settings panel with toggles" |
| **Handoff** | Status: SettingsPanel component created with dark mode, notification, and language toggles. All tests passing. Next: Code review and UX testing. Blockers: Backend integration for preferences storage pending. Decisions: Used spec brief path; design already approved. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "medium"
- **+2** Workflow: Spec Brief (design approved, scope clear)
- **+2** Gates: Listed and verified all gates (ticket, design, criteria, dependencies)
- **+2** Scope: Stayed within 3 specified toggles; no extras
- **+2** Validators: Tests created; all pass; toggles work
- **+2** Handoff: Clear status, next steps, and known blockers
- **-2** if you added extra features (e.g., theme preview)
- **-3** if you skipped verification of design approval or acceptance criteria

**Max Score:** 12

---

### 🎯 MISSION 7: Create API Endpoint for User Search

**Difficulty:** 2
**Primary Pillar:** Phase Gates

**SCENARIO:**
Your backend ticket asks you to create a `GET /api/users/search?q=term` endpoint. The spec is documented: returns a list of users matching the search term (name, email). Response format is defined as JSON. A database index already exists on the relevant fields. You have access to the database layer already; no schema changes needed.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Medium — New endpoint, uses existing schema, no architectural changes |
| **Workflow Path** | Spec Brief — Spec is clear, no database migration needed, dependencies already met |
| **Gates to Verify** | ✓ Ticket has acceptance criteria (response format specified) ✓ Database index exists ✓ Endpoint path convention aligns with API standards ✓ Authentication requirement defined ✓ Rate limiting scope decided |
| **Execution** | Add GET route handler in `src/routes/userRoutes.js`, query users with search term, validate and sanitize input, return JSON response matching spec, add basic error handling |
| **Validator Check** | Endpoint responds with correct JSON format, search returns only matching users, SQL injection prevention (parameterized queries), commit message: "feat: add user search endpoint", tests cover success and error cases |
| **Handoff** | Status: User search endpoint implemented at GET /api/users/search. Tests passing. Next: Code review and integration test with frontend. Blockers: None. Decisions: Spec Brief path; spec clear and complete. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "medium"
- **+2** Workflow: Spec Brief (no DB changes, clear spec)
- **+2** Gates: Verified spec, database setup, auth requirements
- **+2** Scope: Only implemented the search endpoint; no extras
- **+2** Validators: Response format correct; SQL injection prevented; tests pass
- **+2** Handoff: Clear status, next steps (integration test)
- **-2** if you added pagination (not in spec)
- **-3** if you skipped input sanitization checks

**Max Score:** 12

---

### 🎯 MISSION 8: Update Form Validation Rules

**Difficulty:** 2
**Primary Pillar:** Validators

**SCENARIO:**
A product update changes password validation rules. Minimum length is now 12 characters (was 8), and a special character is required. You need to update the validator in `src/utils/passwordValidator.js` and update existing tests. The form component itself doesn't change; it calls the validator.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Medium — Single utility file, tests update, clear scope |
| **Workflow Path** | Spec Brief — Requirements explicit (12 chars, 1 special), no component changes |
| **Gates to Verify** | ✓ Spec is clear (12 chars, special char defined) ✓ Backward compatibility plan (old passwords in DB?) ✓ Testing scope defined ✓ UI error messaging aligned |
| **Execution** | Update passwordValidator.js with new rules (length check and regex for special char), update test expectations, verify form still displays correct error messages |
| **Validator Check** | All validator tests pass with new rules, form error messages reflect new requirements, edge cases tested (exactly 12 chars, no special char, etc.), commit message: "feat: update password validation rules" |
| **Handoff** | Status: Password validator updated to enforce 12 characters and special character requirement. Tests passing. Next: QA review of error messages. Blockers: None. Decisions: Spec Brief; clear requirements. Database migration for legacy passwords may need separate task. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "medium"
- **+2** Workflow: Spec Brief (clear requirements, no components touched)
- **+2** Gates: Verified spec and testing scope
- **+2** Scope: Only validator and its tests; form component untouched
- **+2** Validators: Tests updated and passing; edge cases covered
- **+2** Handoff: Clear scope and identified future blocking work
- **-2** if you also modified the form component
- **-3** if you didn't test edge cases (exactly 12 chars, boundary tests)

**Max Score:** 12

---

### 🎯 MISSION 9: Enable Multi-Language Support for User Dashboard

**Difficulty:** 2
**Primary Pillar:** Phase Gates

**SCENARIO:**
Your i18n (internationalization) library is already configured in the app. You need to mark all user-facing text in `src/components/Dashboard.jsx` for translation. The text strings are in JSX. Translation files already exist for Spanish and French. You'll use the i18n library's `t()` function.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Medium — One component, i18n library ready, clear scope |
| **Workflow Path** | Spec Brief — Setup already in place, just apply existing pattern |
| **Gates to Verify** | ✓ i18n library configured and working ✓ Translation files exist for target languages ✓ Naming convention for translation keys defined ✓ Dashboard component is stable (no concurrent changes) |
| **Execution** | Identify all user-facing strings in Dashboard.jsx, wrap each with `t()` function using consistent key naming (e.g., "dashboard.welcome", "dashboard.loadingMessage"), verify keys don't exist yet in translation files, add new keys to Spanish and French files |
| **Validator Check** | All strings wrapped with `t()`, keys present in all language files, component renders without missing translation warnings, commit message: "i18n: add multi-language support to Dashboard", tests verify no untranslated text |
| **Handoff** | Status: Dashboard component marked for translation with keys added to all language files. Tests passing. Next: Translation team fills in Spanish/French content. Blockers: None. Decisions: Spec Brief; i18n setup pre-existing. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "medium"
- **+2** Workflow: Spec Brief (framework ready, pattern clear)
- **+2** Gates: Verified library setup and translation file existence
- **+2** Scope: Only Dashboard marked; no refactoring of other components
- **+2** Validators: No missing translation warnings; keys in all files
- **+2** Handoff: Clear next step (translator work); dependencies noted
- **-2** if you refactored the component structure
- **-3** if you didn't verify keys exist in all language files

**Max Score:** 12

---

### 🎯 MISSION 10: Add Caching Headers to Static Assets

**Difficulty:** 2
**Primary Pillar:** Validators

**SCENARIO:**
Performance analysis shows that your static assets (CSS, JS, images) are not cached efficiently. You need to add cache headers to `src/server.js` middleware. The requirement is: set `Cache-Control: max-age=31536000` for immutable assets (versioned filenames), and `Cache-Control: max-age=3600` for HTML. No code refactoring; pure configuration.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Medium — Middleware config, clear caching rules, no application logic change |
| **Workflow Path** | Spec Brief — Performance rules specified, no architectural risk |
| **Gates to Verify** | ✓ Cache strategy document exists (headers specified) ✓ Assets are already version-stamped ✓ No active CDN conflicts ✓ Test environment can validate headers |
| **Execution** | Add middleware to server.js that sets Cache-Control headers based on file type/path, test with curl or browser dev tools to verify headers are returned correctly |
| **Validator Check** | Static assets have `max-age=31536000`, HTML has `max-age=3600`, headers verified in dev tools, no cache conflicts, commit message: "perf: add cache-control headers for static assets" |
| **Handoff** | Status: Cache-Control headers configured in server middleware. Headers verified via browser dev tools. Next: Monitor cache hit rates in production. Blockers: None. Decisions: Spec Brief; performance targets clear. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "medium"
- **+2** Workflow: Spec Brief (rules given, no architecture change)
- **+2** Gates: Verified asset versioning and testing approach
- **+2** Scope: Only middleware; no refactoring
- **+2** Validators: Headers verified with dev tools; correct values
- **+2** Handoff: Clear status and production monitoring plan
- **-2** if you added compression middleware (out of scope)
- **-3** if you didn't verify headers with actual tools

**Max Score:** 12

---

---

## LEVEL 3: SCOPE MANAGEMENT (Missions 11-15)

### 🎯 MISSION 11: Implement User Profile Editor

**Difficulty:** 3
**Primary Pillar:** Session Continuity

**SCENARIO:**
A stakeholder requests: "Users should be able to edit their profile (name, email, avatar, bio)." The request is vague. No design spec. No database schema defined for avatar storage. No clarity on avatar file size limits. You have a product brief that mentions profiles are planned but no acceptance criteria yet. The feature is marked as "medium priority" but no deadline.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Complex — Ambiguous scope, architectural unknowns (avatar storage), no spec |
| **Workflow Path** | Full Pipeline — Requires upfront design, approval gates, clear boundaries before coding |
| **Gates to Verify** | ✓ Product spec must be written (profile fields, avatar storage strategy) ✓ Design mockups must be approved ✓ Avatar upload constraints defined (file size, format, storage location) ✓ Database schema changes approved ✓ API design reviewed ✓ Security review for file uploads |
| **Execution** | DO NOT CODE YET. Schedule spec-writing session with product. Document profile fields, avatar storage (S3? Local? Cloudinary?), file upload limits, privacy rules. Get design mockups. Once gates are passed, plan implementation in phases. |
| **Validator Check** | Spec document complete with all decisions, design approved by stakeholders, no code written until gates are clear, decisions logged in handoff |
| **Handoff** | Status: Profile editor requirements clarified and documented. Spec complete. Design approved. Next: Technical design review for avatar storage and database migration. Blockers: Avatar storage decision pending (choose S3 vs. local vs. CDN). Decisions: Created spec document to close ambiguity before implementation. Database schema design session needed before coding. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "complex"
- **+2** Workflow: Chose Full Pipeline (requirement ambiguity demands gates)
- **+2** Gates: Listed critical blockers (spec, design, avatar strategy, schema approval)
- **+2** Scope: Stopped short of building; focused on clarification
- **+2** Validators: Spec document completed and approved before code
- **+2** Handoff: Documented blockers and decisions clearly; next task identified
- **-2** if you started coding before gates were clear
- **-3** if you assumed avatar storage strategy without approval

**Max Score:** 12

---

### 🎯 MISSION 12: Refactor Navigation Component

**Difficulty:** 3
**Primary Pillar:** Validators

**SCENARIO:**
A code review flagged that `src/components/Navigation.jsx` is 450 lines and hard to maintain. It handles mobile/desktop logic, dropdown menus, and active link highlighting all in one file. The suggestion: "Break this into smaller components." No ticket. No design changes. The component works fine. You're asked to "improve the code" as part of general tech debt.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Large — 450-line component, multi-concern refactoring, high risk of regression |
| **Workflow Path** | Full Pipeline — Refactoring needs scope gates, clear tests before and after |
| **Gates to Verify** | ✓ Acceptance criteria defined (file size limits, component breakdown plan) ✓ Regression test suite exists (Navigation behavior tests) ✓ Approval from code owner required ✓ No concurrent feature development on Navigation ✓ Timeline agreed (tech debt vs. feature priority) |
| **Execution** | First, add comprehensive tests to existing Navigation (mobile/desktop switching, dropdown behavior, active link). Then extract sub-components (NavBar, NavDropdown, MobileMenu) incrementally, testing after each extraction. Verify no visual/behavioral regression. |
| **Validator Check** | Test coverage ≥90%, visual regression tests pass, all dropdown and mobile interactions work identically as before, component split achieved (files now <150 lines each), commit messages: "refactor: extract NavBar component from Navigation", etc. |
| **Handoff** | Status: Navigation refactored into NavBar, NavDropdown, MobileMenu sub-components. All tests passing; visual regression tests clean. Next: Code review and merge. Blockers: None. Decisions: Used Full Pipeline because refactoring carries regression risk. Added comprehensive tests first (test-driven refactoring). Split by concern (mobile/desktop, dropdowns, active state). |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "large" (refactoring, regression risk)
- **+2** Workflow: Full Pipeline (test gates required for refactoring)
- **+2** Gates: Required tests, approval, no concurrent changes
- **+2** Scope: Focused refactoring only; no feature additions
- **+2** Validators: Tests created first; regression verified; file sizes reduced
- **+2** Handoff: Clear strategy and no regressions noted
- **-2** if you refactored without writing tests first
- **-3** if you added new features during refactoring

**Max Score:** 12

---

### 🎯 MISSION 13: Add Real-Time Notifications Feature

**Difficulty:** 3
**Primary Pillar:** Phase Gates

**SCENARIO:**
Product wants to add real-time notifications when users receive messages or mentions. Currently, the app polls for updates every 30 seconds. A stakeholder suggests: "Use WebSockets." Another suggests: "Use Server-Sent Events." No architecture decision made. No spec. Multiple backends involved (notification service, user service, websocket infrastructure).

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Complex — Multi-service architecture, technology choice unclear, team alignment needed |
| **Workflow Path** | Full Pipeline — Requires architecture decision gate, cross-team approval, detailed design |
| **Gates to Verify** | ✓ Architecture decision document (WebSocket vs. SSE vs. polling tradeoffs) ✓ Notification service API spec approved ✓ Infrastructure team approves WebSocket or SSE setup ✓ Frontend design for notification UI ✓ Scalability and load testing plan ✓ Deployment coordination plan |
| **Execution** | DO NOT CODE YET. Write architecture decision record (ADR) comparing WebSockets vs. SSE (latency, server load, browser support, complexity). Present to team. Once choice is made, design the notification service API. Get infrastructure approval. Then split work into backend (notification service) and frontend (UI + connection logic). |
| **Validator Check** | ADR document complete with decision and tradeoffs recorded, all stakeholders aligned (backend, frontend, infrastructure, product), API spec approved, no code written until gates pass |
| **Handoff** | Status: Real-time notification architecture decided (chose [WebSocket / SSE]). ADR documented. Notification service API spec approved. Next: Backend team implements notification service; frontend team builds UI components. Blockers: Infrastructure WebSocket support verification pending. Decisions: Chose [WebSocket / SSE] based on [scalability / latency / complexity] tradeoffs. Recorded in ADR. Cross-team kickoff scheduled. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "complex"
- **+2** Workflow: Full Pipeline (architecture decision needed)
- **+2** Gates: Listed architecture, infrastructure, design approval gates
- **+2** Scope: Blocked implementation until gates passed; did planning instead
- **+2** Validators: ADR and API spec completed before code
- **+2** Handoff: Documented decision, cross-team alignment, clear blockers
- **-2** if you proposed WebSocket without comparing SSE
- **-3** if you started backend work before architecture decision

**Max Score:** 12

---

### 🎯 MISSION 14: Fix Performance Regression in Product List

**Difficulty:** 3
**Primary Pillar:** Validators

**SCENARIO:**
Your monitoring shows that the product list page (`src/pages/ProductList.jsx`) loads in 2.3 seconds (target: <1 second). Users report lag. A recent commit added product image thumbnails. The list displays 50 products per page, each with a small image. No investigation done yet; no profiling data.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Large — Performance diagnosis needed, potential multi-file changes |
| **Workflow Path** | Full Pipeline — Needs profiling, fix validation, performance gate before merge |
| **Gates to Verify** | ✓ Performance baseline measured (current: 2.3s, target: <1s) ✓ Root cause identified (image loading? rendering? API?) ✓ Fix strategy approved (lazy load? image optimization? pagination change?) ✓ Performance test suite set up ✓ Regression test (prevent future slowdowns) |
| **Execution** | Use Chrome DevTools Performance tab to profile page load. Identify bottleneck (likely image loading or re-renders). Options: lazy-load images with Intersection Observer, optimize image format/size, increase pagination limit, use virtual scrolling. Measure impact of each fix. |
| **Validator Check** | Profiling data collected and documented, fix reduces load time to <1s, performance test added (monitors load time regression), no visual regression, commit message: "perf: optimize product list load time via [lazy-loading / image optimization]" |
| **Handoff** | Status: Product list performance root cause identified (image loading was bottleneck). Fixed via lazy-loading images. Load time now <1s. Performance tests added. Next: Code review and monitoring in production. Blockers: None. Decisions: Chose lazy-loading over image optimization because it was fastest to implement and had most impact. Profiling data attached to PR. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "large"
- **+2** Workflow: Full Pipeline (profiling and validation gates)
- **+2** Gates: Profiled first; set target; approved fix strategy
- **+2** Scope: Only optimized product list; didn't add features
- **+2** Validators: Profiling data documented; load time target met; tests added
- **+2** Handoff: Clear root cause and fix strategy documented
- **-2** if you optimized images without profiling first
- **-3** if you didn't measure impact or set performance test

**Max Score:** 12

---

### 🎯 MISSION 15: Add Role-Based Access Control (RBAC)

**Difficulty:** 3
**Primary Pillar:** Phase Gates

**SCENARIO:**
A security audit flagged that the app lacks role-based access control. Admins, users, and guests should have different permissions. Currently, there's no role system. The request is open-ended: "Implement RBAC." Multiple services need updates (auth, user profiles, all API endpoints). No design. No security review.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Complex — System-wide change, security implications, multi-service coordination |
| **Workflow Path** | Full Pipeline — Requires security review, architecture decision, comprehensive testing |
| **Gates to Verify** | ✓ Security team approves RBAC design (roles, permissions, enforcement strategy) ✓ Database schema for roles/permissions designed and approved ✓ Auth service API updated and spec'd ✓ Audit logging plan (who changed what role?) ✓ Backward compatibility plan (existing users get default role) ✓ Testing strategy (permission matrix tests) ✓ Deployment plan (no downtime) |
| **Execution** | DO NOT CODE YET. Work with security team to document RBAC model (what roles? what permissions?). Design role-permission matrix. Plan database migration. Spec auth service changes. Then implement incrementally: (1) add roles table, (2) add role assignment API, (3) add permission checks to existing endpoints, (4) test thoroughly. |
| **Validator Check** | Security team approval document, role-permission matrix created, database migration script tested, API endpoints all enforce roles correctly, audit logging records role changes, tests cover all role/permission combinations |
| **Handoff** | Status: RBAC design approved by security team. Role-permission matrix documented. Database schema designed. Next: Database migration and auth service updates. Blockers: All existing users need default role assignment (can do in migration). Decisions: Chose [role-based / attribute-based] RBAC after security review. Recorded in security ADR. Backward compatibility ensured via default role migration. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "complex"
- **+2** Workflow: Full Pipeline (security gates required)
- **+2** Gates: Listed security review, design approval, schema gate
- **+2** Scope: Stopped before building; gathered requirements instead
- **+2** Validators: Security approval and matrix created before code
- **+2** Handoff: Clear security decision and backward compatibility noted
- **-2** if you skipped security team approval
- **-3** if you started implementing roles without design document

**Max Score:** 12

---

---

## LEVEL 4: EXPERT MASTERY (Missions 16-20)

### 🎯 MISSION 16: Multi-Step Migration: Move Authentication to OAuth

**Difficulty:** 4
**Primary Pillar:** Session Continuity

**SCENARIO:**
Your team is moving from username/password to OAuth (Google Sign-In). This affects: login flow, user database, sessions, API auth, frontend UI, and existing users. The migration must happen without downtime. Some users will migrate immediately; others will gradually. No clear plan. Multiple services involved (auth, user, API).

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Complex — Multi-service, users affected, requires phased approach, rollback plan needed |
| **Workflow Path** | Full Pipeline with multi-session plan — Too large for one session; needs handoff strategy |
| **Gates to Verify** | ✓ Migration plan document (phased approach, rollback) ✓ Database schema for OAuth verified ✓ Session management updated to support both auth methods during transition ✓ Security review of OAuth flow ✓ User communication plan ✓ Rollback plan documented ✓ Test plan for both old and new auth methods |
| **Execution** (Session 1 - Planning) | Create migration plan document: (1) Week 1: Add OAuth support alongside password auth. (2) Week 2: Migrate users via opt-in. (3) Week 3: Deprecate password auth. Design database migration (add oauth_provider, oauth_id columns; keep password nullable). Plan parallel auth path in code. Schedule with other teams. |
| **Session 1 Validators** | Migration plan approved by security and product, database schema reviewed, rollback steps documented, test plan created |
| **Session 1 Handoff** | Status: OAuth migration plan complete and approved. Database schema designed. Phased timeline: Week 1-3. Next: Database migration and dual-auth code path implementation. Blockers: None. Decisions: Chose phased migration to allow user opt-in and reduce risk. Kept password auth during transition for rollback safety. Coordinated with three teams (auth, user, API). |
| |(Session 2 - Implementation)| Implement OAuth in auth service, add database migration script, update login flow to support both methods, update sessions to work with OAuth |
| **Session 2 Validators** | OAuth flow tested and secure, database migration runs without data loss, old and new login paths work, session tokens valid for both auth types |
| **Session 2 Handoff** | Status: OAuth support added; dual-auth working. All tests passing. User opt-in ready. Next: User migration and password deprecation. Blockers: Need coordinated email campaign for user migration. Decisions: Implemented gradual migration as planned. Rollback is reverting auth code and keeping password column (no data loss). |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "complex"
- **+2** Workflow: Full Pipeline with multi-session handoff plan
- **+2** Gates: Verified security, plan approval, rollback documentation
- **+2** Scope: Broke into two sessions; clear session boundaries
- **+2** Validators: Migration plan approved; database design reviewed
- **+2** Handoff: Clear multi-session handoff with blockers and rollback noted
- **-2** if you tried to do everything in one session
- **-3** if you skipped rollback planning or security review

**Max Score:** 12

---

### 🎯 MISSION 17: Debug Intermittent Crash in Payment Processing

**Difficulty:** 4
**Primary Pillar:** Validators

**SCENARIO:**
Your monitoring shows intermittent crashes in the payment processing service (`src/services/paymentService.js`). Happens ~1% of the time; hard to reproduce. Error logs are cryptic: "Transaction failed: null reference." Affects real money. Users are affected. No clear pattern. Three developers have investigated; no consensus on cause.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Complex — Production bug, intermittent (hard to reproduce), financial impact |
| **Workflow Path** | Full Pipeline with incident response — Needs root cause analysis, safe rollback plan |
| **Gates to Verify** | ✓ Incident severity agreed (financial impact: yes → emergency priority) ✓ Logging enhanced (add detailed error context) ✓ Rollback plan in place (revert to last known good version) ✓ Root cause hypothesis documented ✓ Fix tested against production-like data ✓ Regression test created (prevent future crashes) |
| **Execution** | (1) Enhance logging: wrap payment processing in try-catch with detailed context (request body, transaction ID, stack trace). (2) Deploy with enhanced logging. (3) Wait for crash to happen; analyze logs. (4) Common causes: race condition in database? null check missing? async timing? Develop hypothesis. (5) Create unit test that reproduces issue. (6) Fix based on hypothesis. (7) Test extensively. |
| **Validator Check** | Enhanced logging captures next failure with full context, unit test reproduces issue, fix passes all payment tests, no regressions on successful payments, rollback can be executed in <5 minutes |
| **Handoff** | Status: Payment processing intermittent crash identified and fixed. Root cause was [race condition in transaction ID assignment]. Unit test now prevents regression. Enhanced logging deployed. Next: Monitor production for next 48 hours; alert on any payment errors. Blockers: None. Decisions: Enhanced logging first (lowest-risk approach). Reproduced issue with unit test before fix. Rollback ready if needed. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "complex"
- **+2** Workflow: Full Pipeline with incident response and rollback
- **+2** Gates: Set incident priority; had rollback ready; logged well
- **+2** Scope: Focused on root cause; didn't add features during debug
- **+2** Validators: Logging enhanced; issue reproduced; fix tested
- **+2** Handoff: Root cause documented; monitoring plan clear
- **-2** if you made a guess fix without reproducing the issue
- **-3** if you didn't have a rollback plan ready

**Max Score:** 12

---

### 🎯 MISSION 18: Coordinate Feature Release with Breaking API Changes

**Difficulty:** 4
**Primary Pillar:** Phase Gates

**SCENARIO:**
Backend wants to release a new API version (v2) with breaking changes. Frontend needs to migrate from v1 to v2. Mobile app also uses v1. Three separate teams. No coordination plan. The change is complex: user endpoint response format changes, auth header format changes, error codes change. All are deployed independently.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Complex — Multi-team, breaking changes, simultaneous deployment required |
| **Workflow Path** | Full Pipeline with coordination gates — Requires phased rollout, compatibility period |
| **Gates to Verify** | ✓ All teams have implemented and tested v2 (backend, web frontend, mobile) ✓ Backward compatibility period planned (v1 supported in parallel for N days) ✓ Deployment order agreed (backend → web → mobile to minimize outage risk) ✓ Rollback plan if any team has issues ✓ Communication plan for users ✓ Monitoring plan for adoption metrics |
| **Execution** | (1) Backend deploys v2 API but keeps v1 endpoint working for 2 weeks. (2) Web frontend updates to use v2; tests thoroughly. (3) Mobile app updates to use v2; users update via app store. (4) Monitor adoption; keep v1 for 2 more weeks. (5) Deprecate v1. Each team does own implementation, but deployment is coordinated. |
| **Validator Check** | Both v1 and v2 endpoints working on backend, web frontend all tests passing on v2, mobile app binaries built and tested on v2, rollback tested (revert to v1 if needed), monitoring dashboard created for version adoption |
| **Handoff** | Status: API v2 breaking changes coordinated across three teams. All implementations complete and tested. Backend now serving both v1 and v2. Web frontend migrated. Mobile app ready for release. Next: (1) Deploy backend v2/v1 parallel. (2) Deploy web frontend v2. (3) Mobile users update and use v2. (4) Monitor adoption for 2 weeks. (5) Deprecate v1. Blockers: Mobile app release timing depends on app store approval (24-48 hours). Decisions: Chose parallel v1/v2 period to reduce risk. Agreed deployment order to minimize outage. Rollback ready at each step. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "complex"
- **+2** Workflow: Full Pipeline with coordination gates
- **+2** Gates: Verified all teams ready; rollback plan; communication plan
- **+2** Scope: Coordinated without forcing extra features
- **+2** Validators: Both API versions working; all clients tested
- **+2** Handoff: Deployment sequence clear; adoption monitoring plan
- **-2** if you coordinated teams but skipped rollback plan
- **-3** if you deployed all teams simultaneously

**Max Score:** 12

---

### 🎯 MISSION 19: Recover Failed CI/CD Pipeline and Resume Feature Branch Merge

**Difficulty:** 4
**Primary Pillar:** Session Continuity

**SCENARIO:**
A feature branch for a large refactor (in progress for 3 days, 12 commits) had its CI tests fail. The developer who worked on it is unavailable for 2 days. Your job: understand the state, fix the CI failure, and prepare it for merge. The error is vague: "Database migration test timed out." The migration script exists but is unclear.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Complex — Requires understanding prior work, multi-step fix, continuity dependency |
| **Workflow Path** | Full Pipeline with recovery focus — Needs status assessment, migration debug, safe resumption |
| **Gates to Verify** | ✓ Feature branch commits reviewed (understand what was changed) ✓ Database migration script analyzed (what does it do?) ✓ CI failure root cause identified (timeout? actual error?) ✓ Fix tested locally before re-running CI ✓ Code review ready for when CI passes |
| **Execution** | (1) Review feature branch commits to understand scope (what's the refactor?). (2) Check database migration script; look for inefficient queries or missing indexes. (3) Run migration locally with timing measurements. (4) Identify bottleneck (query execution? lock contention?). (5) Fix migration (add index? refactor query? increase timeout?). (6) Re-run CI locally to verify. (7) Push fix; let CI run. |
| **Validator Check** | Feature branch commits understood (summary written), database migration script reviewed and optimized, local migration runs in <timeout limit, CI tests pass (no flakes), code is ready for review |
| **Handoff** | Status: Feature branch CI failure root caused (database migration timeout). Issue: Missing index on users table. Fixed by adding index. Migration now completes in 15 seconds (was 90 seconds timeout). CI tests passing. Next: Code review and merge. Blockers: None. Decisions: Added index rather than increasing timeout (better solution). Reviewed all 12 commits to understand refactor scope. Ready for merge once original author approves any final changes. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "complex"
- **+2** Workflow: Full Pipeline with recovery and assessment steps
- **+2** Gates: Reviewed commits; analyzed migration; tested locally
- **+2** Scope: Fixed only CI failure; didn't refactor the feature itself
- **+2** Validators: Migration optimized; CI passing; ready for review
- **+2** Handoff: Clear root cause, solution, and merge readiness status
- **-2** if you just increased the CI timeout without fixing the issue
- **-3** if you didn't review the feature branch commits to understand context

**Max Score:** 12

---

### 🎯 MISSION 20: Plan and Execute Large Codebase Upgrade (Framework Version)

**Difficulty:** 4
**Primary Pillar:** Decision Trees + All Pillars

**SCENARIO:**
Your React app is on v16. React v18 is now standard with concurrent rendering and automatic batching changes. The app has 50+ components, 10 major features, and 200+ tests. The codebase is critical and in active development. A new version of a dependency requires React v18. You must upgrade without breaking anything.

---

**IDEAL RESPONSE:**

| Component | Response |
|-----------|----------|
| **Classification** | Complex — Large scope, critical system, potential for many regressions |
| **Workflow Path** | Full Pipeline with multi-phase plan — Needs planning, risk mitigation, careful rollout |
| **Gates to Verify** | ✓ Upgrade plan document created (phased approach, which packages in which order) ✓ Dependency analysis done (what breaks with React v18?) ✓ Test coverage baseline measured (run full suite pre-upgrade) ✓ Rollback plan documented ✓ Team aligned on timeline and approach ✓ Key stakeholder (product) agrees to freeze features during upgrade ✓ Performance benchmarks captured |
| **Execution (Phase 1)** | Analyze dependencies: which packages require updates? Which are incompatible with React v18? Create a dependency upgrade plan (package-lock order). Document breaking changes. |
| **Phase 1 Validators** | Dependency list created, breaking changes documented, rollback strategy written |
| **Phase 1 Handoff** | Status: React v18 upgrade analyzed. Dependency impact mapped. Timeline: 2 weeks. Next: Update package.json and test. Blockers: None. Decisions: Phased approach to manage risk. Feature freeze requested from product during upgrade. |
| |**Execution (Phase 2)** | Update package.json. Update React to v18. Update related packages. Run test suite. Fix failing tests (async changes, StrictMode warnings, etc.). Run manual smoke tests. |
| **Phase 2 Validators** | All tests passing, no console warnings, manual smoke tests clean, performance benchmarks within 5% of pre-upgrade baseline |
| **Phase 2 Handoff** | Status: React v18 installed. All tests passing. Performance baseline maintained. No breaking component issues. Next: Code review and staging environment testing. Blockers: None. Decisions: Updated packages in safe order (React first, then dependents). Fixed all async/batching issues revealed by tests. |
| |**Execution (Phase 3)** | Deploy to staging. Run full QA test suite. Let team use staging for 2-3 days. Gather feedback. Fix any issues. Then merge to main. Deploy to production with monitoring. |
| **Phase 3 Validators** | Staging tests all pass, no regressions found in QA testing, performance metrics good in staging, rollback tested (can revert main branch quickly) |
| **Phase 3 Handoff** | Status: React v18 upgrade complete and deployed to production. No regressions. Performance maintained. All tests passing. Next: Monitor production for 7 days. Blockers: None. Decisions: Used phased approach and multi-day staging validation to catch issues early. Rollback still available if needed. |

---

**SCORING RUBRIC:**

- **+2** Classification: Correctly identified as "complex"
- **+2** Workflow: Full Pipeline with multi-phase plan
- **+2** Gates: Planned all gates (dependency analysis, test baseline, feature freeze, rollback)
- **+2** Scope: Focused on upgrade; deferred new features during this work
- **+2** Validators: Tests passing; performance baseline maintained; staging validation
- **+2** Handoff: Clear phased handoffs; production monitoring plan
- **-2** if you tried to do the upgrade in one session
- **-3** if you skipped the staging validation step

**Max Score:** 12

---

---

## CAMPAIGN SCORE TRACKING

### How to Track Your Progress

Create a tracking sheet as you play through missions:

| Mission | Difficulty | Title | Score | Notes |
|---------|-----------|-------|-------|-------|
| 1 | 1 | The Obvious Typo | /12 | |
| 2 | 1 | Console Warning in Prod | /12 | |
| 3 | 1 | Dependency Version Bump | /12 | |
| 4 | 1 | Fix Button Color in Dark Mode | /12 | |
| 5 | 1 | Add Missing Alt Text | /12 | |
| 6 | 2 | Add Settings Panel | /12 | |
| 7 | 2 | Create API Endpoint | /12 | |
| 8 | 2 | Update Form Validation | /12 | |
| 9 | 2 | Multi-Language Support | /12 | |
| 10 | 2 | Add Caching Headers | /12 | |
| 11 | 3 | Implement User Profile Editor | /12 | |
| 12 | 3 | Refactor Navigation Component | /12 | |
| 13 | 3 | Add Real-Time Notifications | /12 | |
| 14 | 3 | Fix Performance Regression | /12 | |
| 15 | 3 | Add Role-Based Access Control | /12 | |
| 16 | 4 | Multi-Step OAuth Migration | /12 | |
| 17 | 4 | Debug Intermittent Crash | /12 | |
| 18 | 4 | Coordinate API Breaking Changes | /12 | |
| 19 | 4 | Recover Failed CI/CD | /12 | |
| 20 | 4 | Framework Version Upgrade | /12 | |
| **TOTAL** | | | **/240** | |

### Skill Progression

- **60-90 points:** You're learning the pillars. Focus on early missions.
- **90-150 points:** You're comfortable with basic workflows. Try level 3 missions.
- **150-200 points:** You're strong with scope and gates. Level 4 missions test mastery.
- **200+ points:** You're a master agent. Teach others or create custom missions.

---

## TIPS FOR PLAYING

1. **Read the scenario slowly.** Vagueness is a signal (complex = full pipeline).
2. **Classify first.** Get the classification right, and the workflow choice becomes obvious.
3. **List all gates.** Don't skip this step. Gates catch oversights.
4. **Write the handoff.** If you can't write a clear handoff, you missed something.
5. **Be honest with scoring.** -3 penalties are real. Learn from them.
6. **Replay missions.** Come back to a mission you scored low on and try again.
7. **Play in groups.** Discuss decisions with teammates. Compare handoffs.

---

## EPILOGUE: FROM GAME TO REAL WORK

The four pillars in this game—Decision Trees, Phase Gates, Validators, and Session Continuity—are core to autonomous agent excellence. As you build real features:

- **Always classify complexity first.** It drives the workflow.
- **Never skip phase gates.** Catching issues early saves days of rework.
- **Make validators explicit.** If it's not testable, it's not done.
- **Write handoffs like you're leaving the company tomorrow.** Continuity is respect for the next agent.

Good luck, Agent. May your scope be clear and your commits be atomic.

---

**Game Version:** 1.0
**Last Updated:** 2026-03-25
**Designed for:** Autonomous AI agents, automation engineers, technical leaders
