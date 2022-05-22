(Quick note)
- Create new issue(s) for each task
- Create pull request(s) for each task/issue. A MR for a quick fix might not require an associated issue.
- Only code that has been reviewed can be merged to `develop`
- DO NOT push directly to `develop` even if it's a tiny fix (e.g., typo fix)

The working flow should be:
```
$ git checkout -b [new_branch_name]
$ git add [source_file]
$ git commit -m [a meaningful message/or id of the issue]
$ git push origin [new_branch_name]
```
After passing all tests and reviews:
```
# squash all commits of the current branch into 1 commit
# can either do it manually with git-rebase or
$ git reset $(git merge-base origin/develop $(git branch --show-current))
$ git add -A
$ git commit -m [a meaningful message/or id of the issue]
$ git push origin [your_current_branch]
```
Send a message to the MR thread, saying it's ready for merging, and let the maintainer do his/her job.

# Checklist
- Before clicking `mark as ready` need to check : 
    - Has the latest version been merged from `develop` yet
    - Coding convention 
    - Coding structure: hardcoded values? 
    - Architecture : ? 
    


