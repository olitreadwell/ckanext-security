# data-govt-nz/ckanext-security context
> refreshed 2026-09-06 | upstream default: master @ 2bdc04a

## Identity & policies
- upstream: data-govt-nz/ckanext-security, default branch master, primary language Python (CKAN extension)
- English-first: yes (README/CONTRIBUTING in English; NZ govt org)
- CLA/DCO: none (CONTRIBUTING has no CLA/DCO requirement)
- AI-assisted PR policy: unstated (no AI ban/disclosure found in CONTRIBUTING, README, or org .github; org data-govt-nz/.github absent)
- signed commits required: no
- PR template: none (no .github/PULL_REQUEST_TEMPLATE.md; use pipeline 3-section fallback)
- external tracker: github
- CI: none (no .github/workflows; vetted-repos.jsonl has_ci:false). No test suite in repo.

## Conventions (verified from merged PRs)
- branch naming: mixed. Recent: fix/account-lockout-email-context, feature/robust-password-validation, feature/ivalidators-no-monkey-patch, 2_10_9_compat, refactor_mfa, ckan_2-10_support. No single dominant pattern; type/desc and plain names both used.
- commit style: plain imperative / conventional mix (e.g. "fix(logic): 2.9 mail context;", "feat(logic): more robust password validation;")
- test command: none (no tests in repo)
- lint: flake8 historically (PR #44 "Clean up and prep for Python 3" fix/flake8)
- how outside PRs get merged: responsive. markstuart (maintainer, 115 commits) merges external PRs (JVickery-TBS, wardi, ThrawnCA, twdbben, niallmcandrew-work, RabiaSajjad). Recent merges 2026-02-18.

## Maintainer picture
- active maintainer: markstuart (115 commits). Also active: JVickery-TBS (recent merges #79 #80 #81).
- markstuart actively working on CKAN 2.11 support (open PR #92, branch ckan_2_11_support).
- Areas in flight: CKAN 2.11 support (#92), docs compat (#94), remove six (#93) - avoid duplicating these.

## Issue-area health
- Open issues are mostly feature requests / RFEs, not small bug picks.
- Maintainer-engaged open issue: #75 "Is it possible to include the username in redis connection?" - markstuart replied "Feel free to raise a PR." Small, well-defined: add username support to RedisClient.
- #84 default_user_schema missing image fields - real bug (users can't update profile image), 0 comments, no maintainer engagement.
- #90 CKAN 2.11 Compatibility - large, markstuart working on #92.
- #86 rate limiting on specific URLs - feature request, not small.
- #27 use more defaults - markstuart "see if we can get budget", not approved.

## Gap ledger (dedupe - READ FIRST, never re-pick)
- 2026-09-06 issue #75 (redis username support) - pr-opened (fork PR #1, feature/redis-username). Added optional ckanext.security.redis.username to RedisClient + README. Verified: py_compile + flake8 clean + functional test (username passed when set, None default). No upstream PR/issue covers it.

## Mined gaps (discovered, not yet attempted)
- 2026-09-06 docs: README config block lists redis host/port/db/password but not username; if username support added, document it. status: proposed
