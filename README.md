# No-Proof-No-Merge

A tiny, fail-closed standard: **a pull request cannot be merged unless minimal “Proof” is present**.

This project provides:
- a PR template that includes a **## Proof** section
- a GitHub Actions workflow that fails if “Proof” is missing
- guidance to protect your default branch with **required status checks** and **required reviews**

> Non-goals: This does **not** guarantee fewer bugs/incidents/ROI. It only enforces a *minimal, reviewable proof note*.

## Quick demo (public proof)
1) Open a PR **without** filling the **## Proof** section → the workflow check fails.
2) Edit the PR description and fill **Tests / Evidence / Risk** → the check passes.

## What counts as “Proof” here (minimal)
In the PR body, under **## Proof**, provide:
- `Tests:` what you ran (or `N/A (reason ...)`)
- `Evidence:` link to logs / screenshot / reproduction steps
- `Risk:` low/med/high + blast radius hint
- (optional) `Rollback:` how to revert

Goal: ~30 seconds to fill.

## Install in your repo (high level)
- Add the files in this repository (template + workflow)
- Enable branch protection: require reviews + require status checks
  - Docs: protected branches & status checks

## License
[UNKNOWN]
