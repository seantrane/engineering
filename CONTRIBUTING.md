# Contributing

> Thank you for contributing. Contributions are always welcome, no matter how large or small.

## Table of Contents

- [Guidelines](#guidelines)
- [Pull Requests](#submitting-a-pull-request)
- [Coding Rules](#coding-rules)
- [Working with Code](#working-with-code)
- [File Structure](#file-structure)

---

## Guidelines <a id="guidelines"></a>

As a contributor, here are the guidelines you should follow:

- [Code of conduct](#code-of-conduct)
- [How can I contribute?](#how-can-i-contribute)
- [Using the issue tracker](#using-the-issue-tracker)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Coding rules](#coding-rules)
- [Working with code](#working-with-code)

We also recommend to read [How to Contribute to Open Source](https://opensource.guide/how-to-contribute).

---

## Code of conduct <a id="code-of-conduct"></a>

Please read and follow our [code of conduct](CODE_OF_CONDUCT.md).

---

## How can I contribute? <a id="how-can-i-contribute"></a>

### Improve documentation <a id="improve-documentation"></a>

Consider helping us to improve our documentation by finding _documentation issues_ that need help, and by submitting pull requests for corrections, clarifications, more examples, new features, etc.

Please follow the [Documentation guidelines](STYLE_GUIDES.md#documentation).

### Give feedback on issues <a id=""></a>

Some issues are created without information requested in the [Bug report guideline](#bug-report). Help making them easier to resolve by adding any relevant information.

Issues with the [`type: discussion` label](https://github.com/seantrane/engineering/issues?q=is%3Aissue+is%3Aopen+label%3A%22type%3A+discussion) are meant to discuss the implementation of new features. Participating in the discussion is a good opportunity to get involved and influence the future.

### Fix bugs and implement features <a id=""></a>

Confirmed bug and ready to implement features are marked with the [`help` label](https://github.com/seantrane/engineering/issues?q=is%3Aissue+is%3Aopen+label%3Ahelp). Post a comment on an issue to indicate you would like to work on it and to request help from the team and the community.

---

## Using the issue tracker <a id="using-the-issue-tracker"></a>

The issue tracker is the channel for [bug reports](#bug-report), [features requests](#feature-request) and [submitting pull requests](#submitting-a-pull-request) only. Please use the [Support](README.md#support) and [Get help](README.md#get-help) sections for support, troubleshooting and questions.

Before opening an Issue or a Pull Request, please use the [GitHub issue search](https://github.com/seantrane/engineering/issues?q=) to make the bug or feature request hasn't been [already reported](https://github.com/seantrane/engineering/issues?q=is%3Aopen+) or [fixed](https://github.com/seantrane/engineering/issues?q=reason%3Acompleted).

### Bug report <a id="bug-report"></a>

A good bug report shouldn't leave others needing to chase you up for more information. Please try to be as detailed as possible in your report and fill the information requested in the _[Bug/Issue Template](.github/ISSUE_TEMPLATE/issue_template.md)_.

### Feature request <a id="feature-request"></a>

Feature requests are welcome. But take a moment to find out whether your idea fits with the scope and aims of the project. It's up to you to make a strong case to convince the project's developers of the merits of this feature. Please provide as much detail and context as possible and fill the information requested in the _[Agile Story Template](STORY_TEMPLATE.md)_.

---

## Submitting a Pull Request <a id="submitting-a-pull-request"></a>

Good pull requests whether patches, improvements or new features are a fantastic help. They should remain focused in scope and avoid containing unrelated commits.

**Please ask first** before embarking on any significant pull request (e.g. implementing features, refactoring code), otherwise you risk spending a lot of time working on something that the project's developers might not want to merge into the project.

If you never created a pull request before, then [learn how to submit a pull request (great tutorial)](https://opensource.guide/how-to-contribute/#opening-a-pull-request).

Here is a summary of the steps to follow:

1. [Set up the workspace](#set-up-the-workspace)
2. If you cloned a while ago, get the latest changes from upstream and update dependencies.
3. Create a new topic branch (off the main project development branch) to contain your feature, change, or fix; `git checkout -b <topic-branch-name>`
4. Make your code changes, following the [Coding rules](#coding-rules)
5. Push your topic branch up to your fork; `git push origin <topic-branch-name>`
6. [Open a Pull Request](https://help.github.com/articles/creating-a-pull-request/#creating-the-pull-request) with a clear title and description.

**Tips**:

- Create your branch from `main`.
- Ensure your [git commit messages follow the required format](STYLE_GUIDES.md#git-commit-messages).
- Ensure your scripts are well-formed, well-documented and object-oriented.
- Ensure your scripts are stateless and can be reused by all.
- Update your branch, and resolve any conflicts, before making pull request.
- Fill in [the PR template](.github/PULL_REQUEST_TEMPLATE/pull_request_template.md).
- Do not include issue numbers in the PR title.
- Include screenshots and animated GIFs in your pull request whenever possible.
- Follow the [style guide](STYLE_GUIDES.md) [applicable to the language](STYLE_GUIDES.md#languages) or task.
- Include thoughtfully-worded, well-structured tests/specs. See the [Tests/Specs Style Guide](STYLE_GUIDES.md#tests).
- Document new code based on the [Documentation Style Guide](STYLE_GUIDES.md#documentation).
- End all files with a newline.

---

## Coding rules <a id="coding-rules"></a>

- [Commit message guidelines](STYLE_GUIDES.md#git-commit-messages)
- [Documentation](STYLE_GUIDES.md#documentation)
- [Lint](STYLE_GUIDES.md#lint)
- [Source Code](STYLE_GUIDES.md#source-code)
- [Tests/Specs](STYLE_GUIDES.md#tests)

---

## Working with code <a id="working-with-code"></a>

### Set up the workspace <a id="set-up-the-workspace"></a>

#### Clone the repo into the current directory <a id="clone-repo"></a>

```sh
git clone git@github.com:seantrane/engineering.git engineering && cd engineering
```

#### Install the repo dependencies <a id="install-repo"></a>

```sh
./run install
```

---

## File Structure <a id="file-structure"></a>

```text
engineering/
├─ .github/                                    * Repository configuration directory
│  ├─ ISSUE_TEMPLATE/                          * Templates available when creating an issue
│  │  ├─ issue_template.sh                     * Default issue template
│  │  ├─ [name]_template.sh                    * An issue template
│  │  :
│  │
│  ├─ linters/                                 * Directory for linter configuration files
│  │  ├─ .markdown-lint.yml                    * Markdown-lint config
│  │  ├─ .sass-lint.yml                        * SASS-lint config
│  │  ├─ .tflint.hcl                           * Terraform-lint config
│  │  ├─ .yaml-lint.yml                        * YAML-lint config
│  │  :
│  │
│  ├─ PULL_REQUEST_TEMPLATE/                   * Templates available when creating a pull request
│  │  ├─ pull_request_template.sh              * Default pull request template
│  │  ├─ [name]_template.sh                    * A pull request template
│  │  :
│  │
│  ├─ workflows/                               * Directory for GitHub Actions Workflows
│  │  ├─ delivery.yml                          * Continuous Delivery Workflow
│  │  ├─ deployment.yml                        * Continuous Deployment Workflow
│  │  ├─ integration.yml                       * Continuous Integration Workflow
│  │  ├─ maintenance.yml                       * Maintenance Workflow
│  │  :
│  │
|  ├─ dependabot.yml                           * Dependabot config
|  ├─ labels.json                              * GitHub Labels config
|  ├─ reaction.yml                             * action-reaction config
|  ├─ stale.yml                                * action-stale config
|  └─ super-linter.env                         * Shell support tests
│
├─ bin/                                        * Shell binaries directory
│  └─ [function_name]                          * Shell binaries (typically mapped to respective functions)
│
├─ scripts/                                    * shell scripts directory
│  ├─ functions/                               * Shell functions directory
│  │  ├─ [function_name].sh                    * Shell function (with filename identical to function name)
│  │  :
│  │
|  ├─ load_functions.sh                        * Shell functions (loads all `./scripts/functions/*`)
|  └─ test.sh                                  * Shell support tests
│
├─ .editorconfig                               * keep developers/IDE's in sync
├─ .env.example                                * environment configuration variables template
├─ .gitignore                                  * ignore files for git
├─ CHANGELOG.md                                * changelog autogenerated by `@semantic-release/changelog`
├─ CODE_OF_CONDUCT.md                          * Code of conduct policy
├─ CODEOWNERS                                  * default pull-request reviewers
├─ CONTRIBUTING.md                             * contributing guidelines
├─ docker-compose.yml                          * Docker-compose config
├─ README.md                                   * repository readme
├─ run                                         * Shell script endpoint for running repo shell functions, binaries
├─ sonar-project.properties                    * SonarQube/SonarCloud configuration
└─ STYLE_GUIDES.md                             * Style guides, standards and practices
```

---

#### Happy coding!
