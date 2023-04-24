# Contributing to `<your repository name>`

Thank you for considering contributing to `<your repository name>`, it means a lot to us!\
Below are the most important topics to get you started.

- [Discussions](#discussions)
- [Issue Labels](#issue-labels)
- [Wiki](#wiki)
- [Development Setup](#development-setup)
- [Commit Message Convention](#commit-message-convention)

## Discussions

We use [GitHub Discussions](https://github.com/mhatzl/project-repo-template/discussions) for exchanges with the community.
It is a good place to start if you have any questions.

## Issue Labels

There are two issue labels to help possible contributors to get involved.

- `good first issue` ... This label is used to mark issues that should be easy to implement **without** extensive understanding of the project
- `help-needed` ... This label is used to mark issues, where project members need help to resolve it

## Commit Message Convention

We have precise rules on how we write our git commit messages.\
This leads to **more readable messages** that are easy to follow when looking through the **project history**.
But also, we use git commit messages to automatically get a **change log** using [release-please](https://github.com/googleapis/release-please) from Google.

**Note:** We use `squash merging` for pull requests, so we are able to correct your commit messages, but please try to stick to the convention to make merging easier for us.

## Wiki

We use the [GitHub Wiki](https://github.com/mhatzl/project-repo-template/wiki) for developer related information.
For example, it contains project requirements, decision records, and views/models of the project.

**Note:** Issues for the wiki must be created in this repository, but PRs are handled in a separate [GitHub repository](https://github.com/mhatzl/wiki-repo-template).  

## Development Setup

{{

Provide instructions on how to set up this project for development.

}}

### Commit Message Format

Each commit message consists of a **header**, a **body**, and a **footer**.\
The header has a special format that includes a **type** and a **subject**:

~~~
<type>: <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
~~~

Any line of the commit message cannot be longer than 72 characters, and the header should not be longer than 50 characters!
This allows the message to be easier to read on GitHub as well as in various git tools.

The footer should contain a [closing reference to an issue](https://help.github.com/articles/closing-issues-via-commit-messages/) if any.

**Examples**:

~~~
docs: update changelog to beta.5
~~~

~~~
fix: fix parsing of headings

Heading levels were parsed incorrectly, with an off-by-one error.
~~~

### Revert

If the commit reverts a previous commit, it should begin with `revert: `, followed by the header of the reverted commit. 
In the body it should say: `This reverts commit <hash>.`, where the hash is the SHA of the commit being reverted.

### Type

The commit type must be one of the following:

- **feat** ... Added a new feature
- **fix** ... Fixed a bug of any kind
- **depend** ... Modified an external dependency
- **build** ... Adapted the build system
- **perf** ... Added a code change that improves performance
- **ci** ... Made changes to CI configuration files and scripts
- **test** ... Added one or more test cases
- **refactor** ... Made code changes that neither fixes a bug nor adds a feature
- **style** ... Made code changes that do not affect the semantic of the code
- **doc** ... Made changes that only adds or improves documentation
- **repo** ... Made general changes to the repository (e.g. modified issue templates)
- **revert** ... When reverting a commit, write: `Refs: <comma separated hashes of reverted commits>` in the `[<optional footer>]`
- **chore** ... Made other changes (should only be used for automatically generated commits)

### Subject

The subject contains a succinct description of the change:

- use the imperative, present tense: "change" not "changed" nor "changes"
- don't capitalize the first letter
- no dot `.` at the end

### Body

Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the motivation for the change and contrast this with previous behavior.

### Footer

The footer should contain any information about **Breaking Changes**, and is also the place to
reference GitHub issues that this commit **Closes**.

**Breaking Changes** should start with words `BREAKING CHANGE:` followed by a space.
The rest of the commit message is then used for this.
Also, adding exclamation mark after the commit type indicates breaking change, i.e. `feat!: introduce some new feature`.

### Hooks

Git hooks help to write commit messages according to this convention.
We provide our own commit-msg git hook pre-configured.

To use our commit-msg git hook, copy it into your `.git/hooks/` directory.
Alternatively set our `.hooks/` directory as your git hooks directory with the following shell command: 
`git config core.hooksPath ./.hooks`
