# Contributing Guide

Welcome to the contributing guide for Data Live Online!

In this guide you will get an overview of the contribution workflow from opening an issue, creating a PR, reviewing, and merging the PR.

## Required Tools

### Conda Environment

We test all code using the [Conda package manager](https://github.com/conda/conda) with a code environment based on the latest [Anaconda distribution](https://www.anaconda.com/). Anaconda resolves many issues related to pre-requisites and dependency resolution for many of the open-source libraries that we use.

To get started, visit [https://www.anaconda.com/](https://www.anaconda.com/) and download the latest Anaconda distribution for your operating system. Conda is a part of the Anaconda distribution and will be installed with Anaconda. Be sure to add the conda package manager to your path during the installation dialog.

Once conda is installed, you can run the following commands to ensure that you have the latest version of conda and anaconda. These commands can also be used to update an existing install to the latest stable version:

* `conda update conda`

* `conda update anaconda`

* `conda update -n base -c defaults conda`

Then you can create a new conda environment the following:

```shell
conda create -n PythonData python=3.10 anaconda
```

Note, the name `PythonData` above is the same environment name as used in class. If this enivronment already exists on your machine, you will either need to use a new environment name or remove and re-create the existing environment. This helps us ensure that the code is tested using the latest stable version of conda and anaconda. There are various ways to do this, but take a look at this post on [keeping anaconda updated](https://www.anaconda.com/blog/keeping-anaconda-date) before deciding. We need to ensure that the environment is as close to a fresh new student environment as possible until we can get a docker pipeline in place for testing.

If you want to remove an old environment, you can use `conda env remove -n PythonData --all` and then revist the steps above.

Be sure to activate the environment using `conda activate PythonData`.

### Visual Studio Code

All markdown authoring is created using the Visual Studio Code IDE with the MarkdownLint and Code Spelling extensions enabled. Below are recommended settings used by the team.

#### Recommended VSCode Settings

1. Click the gear (bottom left) in VS Code and select `Command Palette`.

2. Type "Preferences" and select and open, "Preferences: Open User Settings (JSON)".

3. Copy the code below and paste in the `settings.json` file.

    ```json
    {
        "telemetry.enableCrashReporter": false,
        "telemetry.enableTelemetry": false,
        "editor.renderWhitespace": "all",
        "editor.insertSpaces": true,
        "editor.rulers": [
            80,
            120
        ],
        "files.trimTrailingWhitespace": true,
        "files.insertFinalNewline": true,
        "files.trimFinalNewlines": true,
        "[javascript]": {
            "editor.defaultFormatter": "vscode.typescript-language-features",
            "editor.insertSpaces": true,
            "editor.tabSize": 2
        },
        "[typescript]": {
            "editor.defaultFormatter": "vscode.typescript-language-features",
            "editor.insertSpaces": true,
            "editor.tabSize": 2
        },
        "[python]": {
            "editor.defaultFormatter": "ms-python.python",
            "editor.insertSpaces": true,
            "editor.tabSize": 4
        },
        "editor.formatOnType": true,
        "markdownlint.config": {
            "default": true,
            "MD004": {
                "style": "asterisk"
            },
            "MD007": {
                "indent": 4
            }
        }
    }
    ```

#### Recommended VSCode Extensions

The following vscode extensions can be installed from the terminal.

```shell
code --install-extension DavidAnson.vscode-markdownlint
code --install-extension dbaeumer.vscode-eslint
code --install-extension docsmsft.docs-yaml
code --install-extension eamodio.gitlens
code --install-extension esbenp.prettier-vscode
code --install-extension ms-python.python
code --install-extension ms-python.vscode-pylance
code --install-extension ms-toolsai.jupyter
code --install-extension ms-toolsai.jupyter-keymap
code --install-extension ms-toolsai.jupyter-renderers
code --install-extension ms-toolsai.vscode-jupyter-cell-tags
code --install-extension ms-toolsai.vscode-jupyter-slideshow
code --install-extension redhat.vscode-yaml
code --install-extension streetsidesoftware.code-spell-checker
```

## GitHub Setup

Please follow the [official GitHub docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) to setup either ssh or a token for GitHub access to the repositories. 

We also use git-lfs for large files, so you will need [git lfs](https://git-lfs.github.com/) installed and initialized. 

Afterwards, you can clone the repo via:

```shell
git lfs clone git@github.com:coding-boot-camp/DataViz-Lesson-Plans.git
```

## GitHub Workflow

Please see this [document](github-workflow.md) for additional details on our GitHub workflow.

## Pull Request Reviews

TBD

## Git Recommendations and Common Pitfalls

**Important!** Do not use `git rebase`! The current workflow prefers individual commits to the issue branches and then pull requests with squash and merge for the PR.

Please use `git pull` and `git status` frequently.

Avoid using `git add -A` over specifically adding changes with `git add <file or path>`.

VSCode also has great visual tools within the git menu to stage and commit changes.

Use short commit messages that indicate at least the module that was changed.

Example,

```shell
git commit -m "Fixes 3.3.5 activity"
```

The above tells us that module 3, day 3, activity 5 was updated.

Example,

```shell
git commit -m "Updates copyright for modules 3-6"
```
