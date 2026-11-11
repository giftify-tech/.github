<!--
Check the following when creating a pull request:
* Did you add a proper title?
  * Use the conventional commit format (https://www.conventionalcommits.org/en/v1.0.0/#summary)
  * Describe the change that is being made.
  * No punctuation
-->

## Description

<!--
Use the required structure from
https://github.com/giftify-tech/giftify-agent-docs/blob/main/development/guides/pr-descriptions.md:

### Feature overview
Explain the overall feature, problem, or outcome in 2-5 short lines.

### Changes
- Summarize meaningful implementation changes with concise, logically grouped bullets.

### Self-review
Outcome of reviewing this diff against the coding guidelines
(https://github.com/giftify-tech/giftify-agent-docs/blob/main/coding-guidelines/guides/code-review-agent-playbook.md).
One bullet per finding — `🟡 Guideline — what, where — fixed` or `— left because …` — or the single
line "No findings". Evidence the review happened, not a promise that it did.
-->

## 🚀 Deployment

<!--
This section is read at release time — write it for the person deploying, and
keep it updated as the PR evolves. It is scraped by the release-preparation
tooling, so keep the heading exactly as-is.

Two different claims — don't conflate them:
* Nothing to RUN and nothing to KNOW → keep ONLY the "None" line below.
* Nothing to run but something to know (a risk, a rollback note, an adjacent
  gap) → DELETE the "None" line, keep "No deploy steps" plus the relevant
  bullets. A releaser skimming "None" must be safe to stop reading.
Delete whichever remaining lines do not apply.
-->

**None — deploys clean** (nothing to run, nothing to know)

- **No deploy steps** — nothing to run (no migrations, commands or env vars) <!-- keep only alongside Risks/Owner bullets -->
- **Migrations**: <!-- migration names; anything beyond a standard `php artisan migrate`? -->
- **Seeders / commands**: <!-- exact copy-pasteable commands, in order, incl. prompts and answers -->
- **Env vars**: <!-- KEY=example value + which environments -->
- **Cross-repo order**: <!-- e.g. deploy giftify-back-office#470 BEFORE this -->
- **Risks / rollback**: <!-- what could break, how to verify it works, how to undo -->
- **Owner**: <!-- @github-handle who must be present/reachable when this is released -->

## Checklist

### Coding guidelines
- [ ] The `### Self-review` section above records the outcome of reviewing this diff against the [coding guidelines](https://github.com/giftify-tech/giftify-agent-docs/tree/main/coding-guidelines)
      (run it yourself or with an agent — [code review playbook](https://github.com/giftify-tech/giftify-agent-docs/blob/main/coding-guidelines/guides/code-review-agent-playbook.md)); 🔴/🟡 findings are fixed, 🟢 left are listed with a reason
- [ ] I reviewed the complete branch history: each commit contains one logical concept, leaves the codebase working, and carries its relevant tests
- [ ] Fixes, forgotten files, and trailing test commits are folded into the commit they amend

### Code quality
- [ ] I have performed a self-review of my own code.
<!-- Adversarial review: required when the diff hits any trigger listed in
     coding-guidelines/guides/adversarial-review.md#when-one-is-required (money movement,
     shared-state writers, legacy data, auth, data-transforming migrations, …).
     Keep ONE of the next two lines and delete the other. -->
- [ ] Adversarial review run and findings addressed ([when & how](https://github.com/giftify-tech/giftify-agent-docs/blob/main/coding-guidelines/guides/adversarial-review.md))
- [ ] Adversarial review not required — this change is neither risky nor complex
- [ ] I have added tests that prove my fix is effective or that my feature works.
- [ ] I have added tests to cover edge cases.
- [ ] All new and existing tests passed.

### Documentation
- [ ] I have updated the relevant documentation where needed.

### Deployment
- [ ] The 🚀 Deployment section above is accurate and complete (or states "None — deploys clean").
