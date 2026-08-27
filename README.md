# FALL26

Course materials for DATA 201: Intermediate Data Science.

**This repo is read-only for you.** It's the shared "upstream" that all team repos sync from — you don't commit or open Pull Requests here. Your actual work happens in your team's own repo (`hw1-team-*`, `hw2-team-*`, or `final-team-*`, depending on where we are in the semester).

## Getting the latest content

In your team's repo, run the weekly sync:

```
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

(First time only, in a brand new team repo: `git remote add upstream https://github.com/Redlands-DATA201/FALL26.git`)

## One-time setup: clean notebook diffs

This repo is configured to strip notebook outputs from every commit automatically (`nbstripout`), so `.ipynb` merge conflicts come from actual code changes, not from someone re-running a cell. `nbstripout` is already in `requirements.txt`; after installing it, each team member also has to activate it once per clone (this part doesn't happen automatically):

```
nbstripout --install
```

Run that once, right after cloning your team's repo. Everyone on the team needs to run it in their own clone.

Full workflow — branching, Pull Requests, review, the whole cycle — is on the last page of the syllabus and in the printable Git workflow reference.

---
*Last year's FALL25 used a single shared repo with one branch per student. This year each team has its own repo instead — see the syllabus for why.*
