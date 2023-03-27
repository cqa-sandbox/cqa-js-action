# CQA Samples Validation Action

> This is a work in progress. 

---

## Objective

Build a custom action that, given a list of repositories, will 
 - checkout a repository
 - run a (reusable) github action workflow
 - write the (results) artifacts to the local repo

for each repository in the list, where this custom action can itself be triggered based on:
- manual dispatch (browser)
- regular schedule (cron)
- push commits to a branch (e.g., main)
- pull requests (e.g., to main)

---

## Motivation

Add this custom action to the [cqa-dashboard](https://github.com/org-cqa/cqa-dashboard-app)  and have it be triggered to run on a regular schedule (e.g., nightly), followed by a second action that fetches the latest artifacts and rebuilds the dashboard.

 - moves from push to pull model for report updates
 - moves from individual to reusable action for build testing
 - moves from personal access token to org-level or default GITHUB_TOKEN usage

---

## References

 * [Create custom actions](https://docs.github.com/en/actions/creating-actions/about-custom-actions)
 * [Publishing actions in marketplace](https://docs.github.com/en/actions/creating-actions/publishing-actions-in-github-marketplace)
 * [Github Actions Toolkit](https://github.com/actions/toolkit) - with [javascript-action](https://github.com/actions/javascript-action) template
 * [GitHub Reusable Workflows & Custom Actions](https://dev.to/oneadvanced/github-reusable-workflows-and-custom-actions-3cbk)

 ---