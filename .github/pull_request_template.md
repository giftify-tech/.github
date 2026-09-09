<!--
Check the following when creating a pull request:
* Did you add a proper title?
  * Use the conventional commit format (https://www.conventionalcommits.org/en/v1.0.0/#summary)
  * Describe the change that is being made.
  * No punctuation
-->

## Description

<!-- Describe the changes that are being made in this pull request  -->

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
- [ ] I have reviewed my changes against the [coding guidelines](https://github.com/giftify-tech/giftify-agent-docs/tree/main/coding-guidelines)
      (or had an agent check them — see the [code review playbook](https://github.com/giftify-tech/giftify-agent-docs/blob/main/coding-guidelines/guides/code-review-agent-playbook.md))
- [ ] Commits are atomic and rebased — each builds green and carries its own tests

### Code quality
- [ ] I have performed a self-review of my own code.
<!-- Adversarial review: required for risky or complex changes — money movement, shared-state
     writers, legacy predicates/columns, auth, data-transforming migrations, or logic
     intricate enough that bugs could hide in it.
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
