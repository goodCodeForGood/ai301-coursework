# Rubric: is this a good first issue?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever checks
you define here. It ships empty on purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where. Name the source
     (repo-facts block, issue body, comment thread, or the locations in
     references/evidence-guide.md). "The repo" is not a source; "the last
     5 default-branch commit dates" is.
   - Pass condition: a condition someone else could apply and get your
     answer. Prefer thresholds with numbers ("a maintainer commented
     within 30 days") over adjectives ("maintainer is responsive").
   - Weight: `required` (a fail here rejects the issue) or `preferred`
     (never changes the verdict; a nice-to-have that helps rank the
     issues you accept).

2. A verdict rule below the table: how the check grades combine into
   accept or reject, including how `unclear` is treated. The verdict
   space is binary. If you write no rule for `unclear`, the skill treats
   it as fail.

Cover what actually kills first contributions. The lecture named four
families: the maintainer is alive, the repo is in use, the scope fits a
newcomer, and nobody else is already on it. A rubric that ignores a family
will fail eval issues designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| Maintainer activity | The last 5 default-branch commit dates and the most recent maintainer comment in the issue comment thread | At least 1 of the last 5 default-branch commits is within the last 180 days OR a maintainer has commented on the issue within the last 180 days | required |
| Repo activity | The last 5 default-branch commit dates and issue activity in the repository | At least 1 of the last 5 default-branch commits is within the last 180 days | required |
| Newcomer scope | Issue body, labels, and the scope guidance in `references/evidence-guide.md` | The issue describes one bounded change and provides enough context to identify the relevant code, documentation, or configuration; do not reject solely because the issue may touch multiple files or components | required |
| Already claimed | Issue body and comment thread | No contributor is explicitly assigned, has claimed the issue, or is actively working on it in the issue thread | required |


## Verdict rule

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict, they
rank accepted issues; unclear counts as fail." -->

Accept if every required check passes. Preferred checks never change the verdict. If a required check is unclear, treat it as a fail and reject the issue. The verdict is binary: accept or reject.

