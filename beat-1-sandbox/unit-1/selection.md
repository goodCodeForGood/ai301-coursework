# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

https://github.com/codepath/pathreview-ai301-fa26-s1/issues/72


**Verdict output**

```
All three are in scope (codepath/pathreview-ai301-fa26-s1). Graded independently against the four required checks in rubric.md; no preferred checks are defined, so ranking falls to the fit profile alone.

Shared repo evidence (measured against today, 2026-09-23): last 5 default-branch commits are all by Aburke225, newest 2026-09-16 — 7 days old, well inside the 180-day threshold. Repo is not archived. Aburke225 is a COLLABORATOR and opened all three issues.

Ranked read-out

Accepted, in fit order

#53 — PII scrubber fails to redact parenthesized US phone numbers
Best fit: it's the clearest-specified of the three and the narrowest. The body ships a runnable repro with observed output, names the single file (safety/pii_scrubber.py), and lists the four exact tests that must go green — so "done" is unambiguous before you start. The change is one regex pattern in one Python file, which matches a preference for small, focused changes in existing code.

Maintainer activity: pass — collaborator Aburke225 committed 2026-09-16 (7 days ago).

Repo activity: pass — same commit; repo not archived.

Newcomer scope: pass — one bounded change, file and failing tests named.

Already claimed: pass — no assignees, zero comments, no linked PRs.

#72 — verify_password raises UnknownHashError on malformed hashes
Good fit: explicitly scoped at 1–2 hours, two files named, fail-closed behavior stated plainly. Slightly below #53 only because two classmates have already posted full reproductions, so less of the diagnostic work is left to do yourself.

Maintainer activity: pass — same 2026-09-16 commit by Aburke225.

Repo activity: pass.

Newcomer scope: pass — "Verification against a malformed hash should fail closed (return False)", plus remove the xfail marker for H-05.

Already claimed: pass under the Path Review house rule — mikeng07 and DilanCaro both wrote claim comments, but both are author_association: NONE (classmates), no assignees, and the only cross-referenced PR (#1, closed) is an unrelated Unit 1 skill submission.

#68 — Keyword search raises ZeroDivisionError on empty index
Fits, but ranks last: 2–4 hours estimated (the largest of the three) and the fix sits at the boundary with the third-party rank-bm25 library rather than purely in repo code — more unfamiliar surface for the least clear-cut payoff.

Maintainer activity: pass — same 2026-09-16 commit by Aburke225.

Repo activity: pass.

Newcomer scope: pass — one guard in KeywordSearcher.index(), two files named.

Already claimed: pass under the house rule — yulijasso claimed it, but is author_association: NONE; no assignees, no linked PRs.

Rejected: none.

Two notes on the grading. First, a tension worth naming: the rubric's Already claimed condition ("no contributor... has claimed the issue") read literally would fail #72 and #68, but scope.md's Path Review house rule directs that classmates' claim comments don't block, and all claimants are non-members. I applied the house rule; if you disagree, that fix belongs in the rubric, not in this run. Second, the repo has no CONTRIBUTING.md, AI_POLICY.md, or AGENTS.md at root — silence on the AI-contribution surface, which passes, though your rubric has no check for it either way.

[
{
"item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/53",
"checks": [
{"name": "Maintainer activity", "grade": "pass", "evidence": "Last default-branch commit 2026-09-16 by Aburke225 (COLLABORATOR, and the issue's author), 7 days before today 2026-09-23"},
{"name": "Repo activity", "grade": "pass", "evidence": "Newest of last 5 default-branch commits is 2026-09-16, within 180 days; repo archived=false"},
{"name": "Newcomer scope", "grade": "pass", "evidence": "One bounded change: phone regex in safety/pii_scrubber.py, with runnable repro and four named failing tests in tests/unit/test_pii_scrubber.py"},
{"name": "Already claimed", "grade": "pass", "evidence": "assignees: [], comment count 0, no linked PRs in the timeline"}
],
"verdict": "accept"
},
{
"item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/72",
"checks": [
{"name": "Maintainer activity", "grade": "pass", "evidence": "Last default-branch commit 2026-09-16 by Aburke225 (COLLABORATOR), 7 days before today 2026-09-23"},
{"name": "Repo activity", "grade": "pass", "evidence": "Newest of last 5 default-branch commits is 2026-09-16, within 180 days; repo archived=false"},
{"name": "Newcomer scope", "grade": "pass", "evidence": "'Verification against a malformed hash should fail closed (return False), not raise' — two files named, estimated effort 1-2 hours"},
{"name": "Already claimed", "grade": "pass", "evidence": "assignees: []; claims by mikeng07 and DilanCaro are both author_association NONE, which the Path Review house rule says do not block; only cross-ref is unrelated closed PR #1"}
],
"verdict": "accept"
},
{
"item": "https://github.com/codepath/pathreview-ai301-fa26-s1/issues/68",
"checks": [
{"name": "Maintainer activity", "grade": "pass", "evidence": "Last default-branch commit 2026-09-16 by Aburke225 (COLLABORATOR), 7 days before today 2026-09-23"},
{"name": "Repo activity", "grade": "pass", "evidence": "Newest of last 5 default-branch commits is 2026-09-16, within 180 days; repo archived=false"},
{"name": "Newcomer scope", "grade": "pass", "evidence": "One bounded change: guard empty corpus in KeywordSearcher.index(), two files named, estimated effort 2-4 hours"},
{"name": "Already claimed", "grade": "pass", "evidence": "assignees: []; claim by yulijasso is author_association NONE, which the Path Review house rule says does not block; no linked PRs"}
],
"verdict": "accept"
}
]

✻ Baked for 1m 51s · done 12:45 AM

```
Note: The live output above is included verbatim as provided.

---

## Eval iterations

**Run history**

agreement: 17/20 scored items (bar: 18/20: below the bar)

**Issue analysis**

issue-04 — my rubric returned reject, while the gold label was accept. The result was produced because the Newcomer scope check was too strict for that issue. The check treated the issue as outside newcomer scope even though the gold evaluation accepted it. This showed that the scope condition can reject some issues that are still considered suitable first contributions.


**Check rationale**

Newcomer scope — Evidence: issue body and references/evidence-guide.md locations describing the requested files, change, and verification steps. Pass condition: the issue describes a bounded change with named files or components, a clear expected behavior, and a verification path that a newcomer can complete without requiring broad architectural changes.

I kept this check because first contributions need a clearly bounded task and a way to verify the result. Requiring evidence from the issue and specified reference locations makes the decision reproducible instead of relying only on the good first issue label.



**Trade-offs**

The check can reject an issue when the task is still reasonably approachable but spans multiple files or requires learning an unfamiliar component. The mismatch on issue-04 is an example of this trade-off: the rubric rejected it on newcomer scope while the gold label accepted it. I kept the check because removing it would make the rubric less effective at filtering out genuinely broad first issues.


---

## Selection rationale

**Selection rationale**

**1. The issue's fit to my interests and time:** I chose #72 because it is a Python/backend issue involving error handling and authentication-related verification behavior. It is more substantial than a documentation-only task while still being explicitly scoped to about 1–2 hours, which fits my available time.

**2. What the verdict identified correctly, and what I weighed separately:** The verdict correctly identified the active maintainer, active repository, bounded scope, and lack of a blocking maintainer assignment or pull request. I also weighed the opportunity to learn an existing backend verification path and work with tests, which the rubric does not directly measure.

**3. Anticipated difficulty in claiming it:** The issue is marked as good first issue and tier-1, so it is intended to be approachable, but other students may also want it. The technical challenge will be reproducing the malformed-hash failure, understanding the existing verify_password behavior, and making sure malformed hashes return False without changing the behavior for valid hashes and passwords.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
