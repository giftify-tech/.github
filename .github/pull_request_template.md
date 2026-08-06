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

Delete whichever lines do not apply. If the change deploys completely clean,
keep ONLY the "None" line below.
-->

**None — deploys clean** (no migrations, commands, env vars or dependencies)

- **Migrations**: <!-- migration names; anything beyond a standard `php artisan migrate`? -->
- **Seeders / commands**: <!-- exact copy-pasteable commands, in order, incl. prompts and answers -->
- **Env vars**: <!-- KEY=example value + which environments -->
- **Cross-repo order**: <!-- e.g. deploy giftify-back-office#470 BEFORE this -->
- **Risks / rollback**: <!-- what could break, how to verify it works, how to undo -->
- **Owner**: <!-- @github-handle who must be present/reachable when this is released -->

## Checklist

### Code quality
- [ ] I have performed a self-review of my own code.
- [ ] I have added tests that prove my fix is effective or that my feature works.
- [ ] I have added tests to cover edge cases.
- [ ] All new and existing tests passed.

### Documentation
- [ ] I have updated the relevant documentation where needed.

### Deployment
- [ ] The 🚀 Deployment section above is accurate and complete (or states "None — deploys clean").
