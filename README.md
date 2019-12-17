# Githooks

Random assortment of git hooks that are helpful.

## How to install

Enable git templates with `git config --global init.templatedir 'PATH_TO_GITHOOKS_REPO_GITTEMPLATES'`. (e.g. C:\Repos\githooks\git-templates)

Now the hooks will be installed on every new git repo that is created.

### Install on existing Git repos

With the template directory set up, run `git init` on any existing repos to install the hook.

## Usage

### commit-msg

This hook will automatically prepend the JIRA ticket to a commit message. The JIRA ticket is pulled from the branch name.

The following examples show how the hook works with a user written message of `My message`.

| Branch Name | Message Saved With the Commit |
| --- | --- |
| ABC-123 | [ABC-123] My Message |
| ABC-123_Foo | [ABC-123] My Message |
| ABC-123-124 | [ABC-123] [ABC-124] My message |
