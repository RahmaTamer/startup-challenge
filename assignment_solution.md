# Assignment: Advanced Git & CI/CD Challenge - Solutions Guide

## 1. Workflow Architecture & Protection

- **Explanation:** We highly recommend **Trunk-Based Development** for our fast-moving startup. Instead of managing complex, long-lived branches (like in GitFlow) which heavily leads to painful merge conflicts, developers merge their small, frequent updates directly into a single `main` branch. This speeds up production delivery and ensures continuous integration.
- **Enforced GitHub Branch Protection Rules:**
  1. _Require a pull request before merging:_ Disables direct pushing to `main`, ensuring all code goes through review.
  2. _Require status checks to pass before merging:_ Ensures that our automated CI integration pipeline must pass successfully before any code is merged.

---

## 2. History Cleanup (Interactive Rebase)

- **Explanation:** During an interactive rebase:
  - `pick`: Retains the commit as-is in the project history.
  - `squash`: Combines the commit's changes into the previous commit, melting multiple messy commits (like typos or WIPs) into one clean commit.
- **Exact Git Command:**
  ```bash
  git rebase -i HEAD~5
  ```
