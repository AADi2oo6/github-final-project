# Coursera Introduction to Git and GitHub — Final Project Submission

This document contains the verified, paste-ready answers for all nine questions of the Coursera "Introduction to Git and GitHub" Final Project course assessment.

- **GitHub Username:** `AADi2oo6`
- **Part 1 Repository (Questions 1–5):** `https://github.com/AADi2oo6/github-final-project`
- **Part 2 Fork Repository (Questions 6–9):** `https://github.com/AADi2oo6/mcino-Introduction-to-Git-and-GitHub`
- **Upstream Repository:** `https://github.com/ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub`

---

## Question 1: README.md Public URL

### Public URL
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

## Question 2: LICENSE Public URL and Apache 2.0 Verification

### Public URL
```
https://github.com/AADi2oo6/github-final-project/blob/main/LICENSE
```

### Verification of Apache License 2.0 Sections
The file named exactly `LICENSE` is located at the root of the repository and contains the complete canonical Apache License 2.0 text, including all nine numbered sections:
1. `1. Definitions`
2. `2. Grant of Copyright License`
3. `3. Grant of Patent License`
4. `4. Redistribution`
5. `5. Submission of Contributions`
6. `6. Trademarks`
7. `7. Disclaimer of Warranty`
8. `8. Limitation of Liability`
9. `9. Accepting Warranty or Additional Liability`

---

## Question 3: CODE_OF_CONDUCT.md Public URL and Required Headings

### Public URL
```
https://github.com/AADi2oo6/github-final-project/blob/main/CODE_OF_CONDUCT.md
```

### Verification of Required Headings
The file is named exactly `CODE_OF_CONDUCT.md` at the repository root and adheres to the Contributor Covenant v2.0 standard, containing all seven required headings:
- `## Our Pledge`
- `## Our Standards`
- `## Enforcement Responsibilities`
- `## Scope`
- `## Enforcement`
- `## Enforcement Guidelines`
- `## Attribution`

---

## Question 4: CONTRIBUTING.md Public URL and Exact Required Sentence

### Public URL
```
https://github.com/AADi2oo6/github-final-project/blob/main/CONTRIBUTING.md
```

### Required Sentence
The exact required sentence appears as the leading guideline in the document:
```
All contributions, bug reports, bug fixes, documentation improvements, enhancements, and ideas are welcome.
```

---

## Question 5: simple-interest.sh Public URL and Script Description

### Public URL
```
https://github.com/AADi2oo6/github-final-project/blob/main/simple-interest.sh
```

### Description
- **Language / Environment:** Bash shell script (`#!/bin/bash`).
- **File Permissions:** Executable (`chmod +x`).
- **Inputs:** Prompts the user interactively for:
  - `p` — Principal amount
  - `r` — Annual rate of interest
  - `t` — Time period in years
- **Formula:** Calculates the simple interest dividing by 100:
  ```bash
  s=`expr $p \* $t \* $r / 100`
  ```
- **Output:** Displays the computed simple interest to the user.
- **Verification:** Tested with principal = 1000, rate = 5, time = 2; output correctly returned 100.

---

## Question 6: Fork Verification (`forked-repo`)

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

## Question 7: Merge bug-fix-typo into main (`merge_branches`)

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

## Question 8: Real Pull Request Verification (`bug-fix-revert`)

### Pull Request Information
- **Pull Request Number:** `13003`
- **Pull Request URL:** `https://github.com/ibm-developer-skills-network/mcino-Introduction-to-Git-and-GitHub/pull/13003`
- **Head Branch:** `AADi2oo6:bug-fix-revert`
- **Base Branch:** `ibm-developer-skills-network:main`
- **Title:** `Fix simple interest formula in README`
- **Automated Verification Note:** Upon submission, IBM Developer Skills Network automated actions verified and confirmed completion with comment: *"Congratulations! You have completed the lab. Closing for maintainence purpose."*

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

## Question 9: Branch Listing (`github-branches`)

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
