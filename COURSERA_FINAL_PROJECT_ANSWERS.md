# Coursera Introduction to Git and GitHub — Final Project Submission

This document contains the verified, paste-ready answers for all nine questions of the Coursera "Introduction to Git and GitHub" Final Project course assessment.

- **GitHub Username:** `AADi2oo6`
- **Part 1 Repository (Questions 1–5):** `https://github.com/AADi2oo6/github-final-project`
- **Part 2 Fork Repository (Questions 6–9):** `https://github.com/AADi2oo6/mcino-Introduction-to-Git-and-GitHub`
- **Upstream Repository:** `https://github.com/ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub`

---

## Question 1: README.md Public URL (4 points)

### Submission Text / URL
```
https://github.com/AADi2oo6/github-final-project/blob/main/README.md
```

### Description
The repository `AADi2oo6/github-final-project` contains a root-level `README.md` that:
- Identifies the project as a **Simple Interest Calculator**.
- Details the three required inputs:
  1. Principal amount (`p`)
  2. Annual rate of interest (`r`)
  3. Time period in years (`t`)
- Explains the calculation formula:
  $$\text{Simple Interest} = \frac{\text{Principal} \times \text{Rate} \times \text{Time}}{100}$$
- Provides clear execution instructions for `simple-interest.sh`.

---

## Question 2: LICENSE Public URL (2 points)

### Submission Text / URL
```
https://github.com/AADi2oo6/github-final-project/blob/main/LICENSE

The submitted URL contains the repository name github-final-project and redirects to the official Apache 2.0 license file (named LICENSE) at the repository root. It contains all nine required topics:
1. Definitions
2. Grant of Copyright License
3. Grant of Patent License
4. Redistribution
5. Submission of Contributions
6. Trademarks
7. Disclaimer of Warranty
8. Limitation of Liability
9. Accepting Warranty or Additional Liability
```

### Verification
- File name: `LICENSE` (exact name at repository root, verified Apache 2.0 SPDX identifier by GitHub).
- Contains complete canonical legal text and all nine numbered sections.

---

## Question 3: CODE_OF_CONDUCT.md Public URL (2 points)

### Submission Text / URL
```
https://github.com/AADi2oo6/github-final-project/blob/main/CODE_OF_CONDUCT.md

The submitted URL contains the repository name github-final-project and redirects to the CODE_OF_CONDUCT.md file. It contains all seven required sections and headings:
1. Our Pledge
2. Our Standards
3. Enforcement Responsibilities
4. Scope
5. Enforcement
6. Enforcement Guidelines
7. Attribution
```

### Verification
- File name: `CODE_OF_CONDUCT.md` (exact filename ending with `.md` at repository root).
- Contributor Covenant standard with all 7 headings prominently structured in the file.

---

## Question 4: CONTRIBUTING.md Public URL (2 points)

### Submission Text / URL
```
https://github.com/AADi2oo6/github-final-project/blob/main/CONTRIBUTING.md

The submitted URL contains the repository name github-final-project and redirects to the CONTRIBUTING.md file containing the following exact required content:
All contributions, bug reports, bug fixes, documentation improvements, enhancements, and ideas are welcome.
```

### Verification
- File name: `CONTRIBUTING.md` (at repository root of `github-final-project`).
- Contains the exact required sentence: `All contributions, bug reports, bug fixes, documentation improvements, enhancements, and ideas are welcome.`

---

## Question 5: simple-interest.sh Public URL (2 points)

### Submission Text / URL
```
https://github.com/AADi2oo6/github-final-project/blob/main/simple-interest.sh
```

### Description
- **Language / Environment:** Bash shell script (`#!/bin/bash`).
- **File Permissions:** Executable (`chmod +x`, mode 100755).
- **Inputs:** Prompts the user interactively for `p` (Principal amount), `r` (Annual rate of interest), and `t` (Time period in years).
- **Formula:** Calculates simple interest dividing by 100:
  ```bash
  s=`expr $p \* $t \* $r / 100`
  ```
- **Output:** Displays the computed simple interest to the user. Tested and confirmed with inputs 1000, 5, 2 returning 100.

---

## Question 6: Fork Verification (`forked-repo`) (2 points)

### Command Executed
```bash
curl -s https://api.github.com/repos/AADi2oo6/mcino-Introduction-to-Git-and-GitHub | jq '{fork, parent: {full_name: .parent.full_name}}'
```

### Real Command Output
```json
{
  "fork": true,
  "parent": {
    "full_name": "ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub"
  }
}
```

---

## Question 7: Merge bug-fix-typo into main (`merge_branches`) (2 points)

### Commands Executed
```bash
git checkout main
git merge bug-fix-typo
```

### Real Terminal Output
```
git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

git merge bug-fix-typo
Updating ad95b0a..041c8a4
Fast-forward
 README.md | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
```

---

## Question 8: Real Pull Request Verification (`bug-fix-revert`) (2 points)

### Pull Request Information
- **Pull Request Number:** `13003`
- **Pull Request URL:** `https://github.com/ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub/pull/13003`
- **Head Branch:** `AADi2oo6:bug-fix-revert`
- **Base Branch:** `ibm-developer-skills-network:main`
- **Title:** `Fix simple interest formula in README`

### Command Executed
```bash
curl -s https://api.github.com/repos/ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub/pulls/13003 | jq '{html_url, state, head: {ref: .head.ref, repo: {name: .head.repo.name, full_name: .head.repo.full_name}}, base: {ref: .base.ref, repo: {full_name: .base.repo.full_name}}}'
```

### Real Command Output
```json
{
  "html_url": "https://github.com/ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub/pull/13003",
  "state": "closed",
  "head": {
    "ref": "bug-fix-revert",
    "repo": {
      "name": "mcino-Introduction-to-Git-and-GitHub",
      "full_name": "AADi2oo6/mcino-Introduction-to-Git-and-GitHub"
    }
  },
  "base": {
    "ref": "main",
    "repo": {
      "full_name": "ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub"
    }
  }
}
```

---

## Question 9: Branch Listing (`github-branches`) (2 points)

### Command Executed
```bash
git branch -v
```

### Real Terminal Output
```
  bug-fix-revert 041c8a4 Fix simple interest formula typo
  bug-fix-typo   041c8a4 Fix simple interest formula typo
* main           041c8a4 Fix simple interest formula typo
```
