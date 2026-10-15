# By hand, then the agent

Fill this in during Module 2.3.

## What I did by hand
I ran each step myself: git init, created a file, git add and git commit, created a branch with git switch -c, edited a file and committed, pushed with git push, then opened and merged the pull request on github.com.

## What the agent did
I gave Claude Code one instruction per step and read each result before the next. It ran git init, created README.md and committed ("Add README"), made the update-readme branch, added a line and committed ("Add second line to README"), then added the remote and pushed. Differences from my manual run are:
- It added a "Co-Authored-By: Claude Opus 5.5" line to both commit messages.
- It pushed update-readme before main, which risked making update-readme the default branch. It warned me to check this in settings.
- It tried to open the PR with gh, which isn't installed, so it gave me a compare link and I created and merged the PR in the browser

## One thing the agent could have done better, and what I changed
I asked for "a README with a shorter line about this project." git show bbd6931 shows it created 3 lines. The heading and blank line weren't requested. git show 227c2ad shows the second commit only added one line, and nothing was removed. I checked that only README.md changed in both commits and in the PR's Files changed tab, and that each commit message matched its diff. I accepted the extra heading because it's harmless, but noted it as a change I didn't ask for.

If you found nothing to correct, show the diff you read and say what you checked in it.

## What I would check first next time
The push order and default branch, and whether the agent adds anything to commit messages, like the co-author line. I'd also run git show HEAD right after each commit instead of reviewing everything at the end.
