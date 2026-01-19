# Remote Repository Setup

## Current Remotes
backup	git@github.com:vovkadenisov/techstart-api-backup.git (fetch)
backup	git@github.com:vovkadenisov/techstart-api-backup.git (push)
backup	git@github.com:vovkadenisov/techstart-api.git (push)
origin	git@github.com:vovkadenisov/techstart-api.git (fetch)
origin	git@github.com:vovkadenisov/techstart-api.git (push)
origin	git@github.com:vovkadenisov/techstart-api-backup.git (push)

## Tracking Branches
  develop d460558 Finalize remote repositories assignment
* main    4981eb0 [origin/main: ahead 2] Finalize remote repositories assignment

## Fork Workflow Summary
- Original repository: https://github.com/vovkadenisov/awesome-calculator
- Fork repository: https://github.com/vovkadenisov1/calculator-fork
- Upstream configuration: git remote add upstream git@github.com:vovkadenisov/awesome-calculator.git

## Backup Strategy
- Primary remote: origin
- Backup remote: backup
- Sync command: git push origin --all && git push origin --tags

## Lessons Learned
Важно разделять роли remotes: upstream для получения изменений, origin для своей публикации. Tracking веток (git branch -u ...) убирает путаницу, а fetch --prune помогает держать refs чистыми. Несколько push URL позволяют зеркалировать изменения в backup одним push.
