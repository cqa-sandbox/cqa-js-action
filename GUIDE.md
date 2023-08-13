# Custom CQA-JS-ACTION 

Following the [GitHub Docs](https://docs.github.com/en/actions/creating-actions/creating-a-javascript-action) guidance, in conjunction with the new [VS Code Extension for Actions](https://marketplace.visualstudio.com/items?itemName=github.vscode-github-actions) for authoring and debugging help.

## Pre-Requisites

 * Use Node.js 16.x (LTS) > `nvm use 16`
 * Create new repo, initialize > `npm init -y`
 * Create new action file > `touch action.yml`
 * Add initial content to `action.yml` > [use example](https://docs.github.com/en/actions/creating-actions/creating-a-javascript-action#creating-an-action-metadata-file) 

 ```yaml
name: 'CQA Samples Validation Action'
description: 'Run automated build & deploy tests on identified JS sample repos'

inputs:
  config-path:
    description: 'Path to the configuration file'
    required: true
    default: 'config.json'
  artifacts-path:
    description: 'Top folder for storing run artifacts'
    required: true
    default: 'cqa-artifacts'

outputs:
  time: # unique run timestamp (useful ID)
    description: 'The time we last ran this action!'
  artifacts: # folder containing run results
    description: 'The folder containing the run results'

runs:
    using: 'node16'
    main: 'index.js'
```