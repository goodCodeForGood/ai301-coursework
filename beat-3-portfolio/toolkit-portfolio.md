*Toolkit Portfolio*
*Building an AI Tool for Open Source Issue Selection*
**Overview**

For my AI Open Source Capstone, I built issue-select, an AI tool that helps developers find suitable open-source issues. I created my own evaluation rubric with four criteria: maintainer activity, repository activity, newcomer scope, and whether an issue had already been claimed. I tested the tool against 20 labelled cases and achieved 17/20 agreements (85%), slightly below the target of 18/20. This helped me understand why evaluating AI decisions is just as important as building the tool.

**What happened**
***Building and using the tool***

I wanted to make open-source issue selection more structured instead of relying entirely on AI recommendations. I created four checks:

- Maintainer activity: whether project maintainers were active.
- Repository activity: whether the repository was active and maintained.
- Newcomer scope: whether the task was manageable for a beginner.
- Already claimed: whether another qualifying contributor had claimed the issue.

I then tested the tool on three issues from the Path Review repository:

- Issue #53: A PII scrubber bug involving phone number redaction. Ranked first because it had a clear reproduction and specific tests.
- Issue #72: A malformed password hash issue. Ranked second, but I selected it because I was interested in Python backend development.
- Issue #68: An empty-index search error. Ranked third because it involved an unfamiliar third-party library.

Selected issue #72

**Evaluating the results**

On September 23, 2026, I ran the tool against 20 labelled cases using a pinned Sonnet model.

My actual results were:

Total cases: 20
Agreement: 17/20 (85%)
Target: 18/20 (90%)

Category breakdown:
claimed:       4/4
clear-accept:  6/8
dead-repo:     3/3
policy:        1/1
scope:         3/4


There were three disagreements:

Case	  Expected	Actual
issue-04	Accept	Reject
issue-15	Reject	Accept
issue-19	Accept	Reject

Issues 04 and 19 were rejected because my newcomer-scope check was too strict. Issue 15 showed the opposite problem: the tool accepted an issue that should have been rejected.

One condition in my rubric was:

The issue describes a bounded change with named
files or components, a clear expected behavior,
and a verification path that a newcomer can complete.


I kept this criterion because I believe first contributions should have clear requirements and verification steps. However, I recognized that it could exclude approachable issues involving multiple files or unfamiliar components.

I documented these limitations in my evaluation notes but did not complete a revised rubric or another evaluation run. Therefore, 17/20 remains my final recorded result.

**Limitations and what's next**

The main limitation of my tool is that its newcomer-scope check can be too restrictive, while issue-15 showed that it can also accept unsuitable issues. I also tested it on only 20 labelled cases, so it needs more evaluation across different repositories.

My next step would be to investigate the disagreements, refine the rubric, and run another evaluation to see whether the results improve.

My biggest takeaway is that building an AI tool is only part of the work. Testing its decisions, understanding its mistakes, and being honest about its limitations are what make it useful and trustworthy.
