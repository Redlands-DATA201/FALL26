# FALL26

Course materials for DATA 201: Intermediate Data Science.

You have **two repos** this semester and they do two different jobs.

| | |
|---|---|
| **`sandbox-yourusername`** | Yours. A full copy of this repo. Work through the lectures here, run the cells, break things. Never graded, nobody else sees it. |
| **`team-yourteam`** | Your team's. Only `Week01` through `Week12` folders. Homework goes in that week's folder, on a branch, through a Pull Request. This is what gets graded. |

**This repo (`FALL26`) is read-only for you.** It is the shared "upstream" that every
sandbox pulls from. You do not commit or open Pull Requests here.

Full instructions are in **Your Two Repos**, and the workflow page at the end of the
syllabus.

## Getting the latest content

New notes land in your **sandbox**, not in your team's repo:

```
git checkout main
git fetch upstream
git merge upstream/main
```

If git reports a conflict in one of my files, it just means you changed something I also
changed. Nothing in your sandbox is graded, so take my version and move on:

```
git checkout upstream/main -- <the file it named>
```

(First time only, right after cloning your sandbox:
`git remote add upstream https://github.com/Redlands-DATA201/FALL26.git`)

## Handing in homework

The `HW_day<N>.ipynb` files here are where you work the problems, in your sandbox. What
you hand in is a **separate write-up notebook** that you create in your team's repo, in
that week's folder.

You keep one branch in the team repo all semester, named after you:

```
git checkout main
git pull origin main
git checkout yourname
git merge main
```

Work in that week's folder, commit, push, and open a Pull Request into `main`. A teammate
reviews it, then it gets merged. You cannot commit to `main` directly.

## One-time setup: clean notebook diffs

Both repos strip notebook outputs from every commit automatically (`nbstripout`), so
`.ipynb` conflicts come from real code changes and not from someone re-running a cell.
`nbstripout` is in `requirements.txt`, but each person has to activate it once **per
clone**:

```
nbstripout --install
```

Run it in your sandbox and again in your team's repo. If you ever get a notebook conflict
with thousands of nonsense lines in it, this is the step that got skipped.

---
*Fall 2025 used a single shared repo with one branch per student. Earlier in Fall 2026 we
used one team repo that also held the course notes. Splitting the notes into a personal
sandbox is what stops my updates from turning into your team's merge conflicts.*
