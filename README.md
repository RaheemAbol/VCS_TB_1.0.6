# VCS_TB_1.0.6
---

### 🎟️ Ticket #006 – **"Refactor Pass: Branching, PR, and Merge"**

#### 🎯 Objective

You’ve been assigned a small **refactor pass**. Do the work on a feature branch, **open a Pull Request (PR)** on GitHub, merge it there, and then **sync your local `main`**. This mirrors a standard team workflow.

> 🔁 Assumes default branch is `main`. If your repo uses `master`, substitute accordingly.

---

### 📝 Tasks

#### 🌿 1) Start Clean on `main`

From your project repo (`project-hub/`):

```bash
git checkout main
git pull origin main
```

#### 🧵 2) Create & Switch to a Feature Branch

```bash
git checkout -b refactor-pass-1
```

#### 📝 3) Make the Change (Refactor Log Example)

Create a file and add some text to the file, make a meaningful change to commit:

```bash
mkdir src
touch refactor_log.md
(add text) "- Renamed utility methods for clarity
- Simplified main class structure
- Removed unused imports" > src/refactor_log.md
```

Stage and commit:

```bash
git add src/refactor_log.md
git commit -m "Add refactor_log.md documenting refactor steps"
```

#### ☁️ 4) Push Feature Branch to GitHub

```bash
git push -u origin refactor-pass-1
```

#### 🔀 5) Open a PR on GitHub (GUI)

* Go to your repo on GitHub
* **Base:** `main`  ←  **Compare:** `refactor-pass-1`
* Title & describe the change
* Create PR → request review if needed → **Merge** (Merge/Squash/Rebase per team policy)

> 💡 If CI checks or reviews are required, ensure they pass before merging.

#### 🔄 6) Sync Local `main` After Merge

```bash
git checkout main
git pull origin main
```

#### 🧹 7) Clean Up Branches (Optional, Recommended)

On GitHub: click **Delete branch** after merge.
Locally:

```bash
git branch -d refactor-pass-1
git fetch -p
# if needed (not auto-deleted remotely):
git push origin --delete refactor-pass-1
```

---

### ✅ Completion Checklist

* [ ] Local `main` updated before branching (`git pull origin main`)
* [ ] Feature branch created: `refactor-pass-1`
* [ ] Refactor change added & committed on the branch
* [ ] Branch pushed to GitHub with upstream tracking
* [ ] PR opened: **base** `main` ← **compare** `refactor-pass-1`
* [ ] PR merged on GitHub
* [ ] Local `main` pulled to include the merge
* [ ] Feature branch deleted locally/remotely (optional)

---

Want me to turn this into a **printable one-pager** or a **class handout** with screenshots/placeholders for GitHub steps?
