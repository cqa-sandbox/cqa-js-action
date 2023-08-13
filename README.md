# CQA Samples Validation Action

> This is a work in progress. 

---

## Objective

Build a custom action that can:
 1. checkout a target `samples` repository
 2. validate the default _build_ workflow
 3. run optional _test_ workflows
 4. write result _artifacts_ to a specified folder in local repo

where the action is invoked with:
 - inputs = config file listing one or targets
 - outputs = artifacts folder (with each target in a subfolder)

and action can be triggered by:
 - manual dispatch (browser)
 - regular schedule (cron)
 - push commits to branch (change to config file)
 - pull requests (change to config file)

---

## Motivation

Add this custom action to the [cqa-dashboard](https://github.com/org-cqa/cqa-dashboard-app)  and have it be triggered to run on a regular schedule (e.g., nightly), followed by a second action that fetches the latest artifacts and rebuilds the dashboard.

 - moves from push to pull model for report updates
 - moves from individual to reusable action for build testing
 - moves from personal access token to org-level or default GITHUB_TOKEN usage

---

## References

 * [Create custom actions](https://docs.github.com/en/actions/creating-actions/about-custom-actions)
 * [Create JS action](https://docs.github.com/en/actions/creating-actions/creating-a-javascript-action) - w/ GitHub Actions Toolkit Node.js module
 * [Publishing actions in marketplace](https://docs.github.com/en/actions/creating-actions/publishing-actions-in-github-marketplace)
 * [Github Actions Toolkit](https://github.com/actions/toolkit) - with [javascript-action](https://github.com/actions/javascript-action) template
 * [GitHub Reusable Workflows & Custom Actions](https://dev.to/oneadvanced/github-reusable-workflows-and-custom-actions-3cbk)
 * [GitHub Actions for VS Code](*https://github.blog/2023-03-28-announcing-the-github-actions-extension-for-vs-code/)

 ---