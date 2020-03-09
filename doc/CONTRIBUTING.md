# Contributing Guide

It is warmly welcomed if you have interest to contribute to this project and help make it even better than it is today! The following is a set of guidelines for contributing.

- [Code of Conduct](#coc)
- [Submitting an Issue](#issue)
- [Submitting a Pull Request](#pr)

## <a name="coc"></a> Code of Conduct

We have adopted a [Code of Conduct][coc] to help us keep this project open and inclusive. Please read the full text so that you can understand what actions will and will not be tolerated.

## <a name="issue"></a> Submitting an issue

If you have any questions or feature requests, please feel free to [submit an issue][new-issue].

Before you submit an issue, consider the following guidelines:

- Please search for related issues. Make sure you are not going to open a duplicate issue.
- Please specify what kind of issue it is and explain it in the title or content, e.g. `feature`, `bug`, `documentation`, `discussion`, `help wanted`... The issue will be tagged automatically by the robot of the project(Menbotics). See [supported issue labels][issue-label].

To make the issue details as standard as possible, we setup an [Issue Template][issue-template] for issue reporters. Please be sure to follow the instructions to fill fields in template.

There are a lot of cases when you could open an issue:

- bug report
- feature request
- performance issues
- feature design
- help wanted
- doc incomplete
- test improvement
- any questions on project
- and so on

Also we must remind that when filling a new issue, please remember to remove the sensitive data from your post. Sensitive data could be password, secret key, network locations, private business data and so on.

## <a name="pr"></a> Submitting a Pull Request

To help you get your feet wet and get you familiar with our contribution process, we have collected some [good first issues][good-first-issues] that contain bugs or small features that have a relatively limited scope. This is a great place to get started.

Before you submit your Pull Request (PR), consider the following guidelines.

### 1. Claim an issue

Be sure that an issue describes the problem you're fixing, or documents the design for the feature you'd like to add.

If you decide to fix an issue, please be sure to check the comment thread in case somebody is already working on a fix. If nobody is working on it at the moment, please leave a comment with `/self-assign` stating that you intend to work on it so other people don't accidentally duplicate your effort. The robot of the project(Menbotics) will set assignees of the issue to yourself automatically.

```shell
/self-assign
```

If somebody claims an issue but doesn't follow up for more than two weeks, it's fine to take over it but you should still leave a comment.

### 2. Fork and clone the repository

Visit [2020NCOV/ncov-report-mini-program-server][repo] repo and make your own copy of the repository by **forking** it.

And **clone** your own copy of the repository to local, like :

```shell
# replace the XXX with your own user name
git clone git@github.com:XXX/ncov-report-mini-program-server.git
cd ncov-report-mini-program-server
```

### 3. Create a new branch

Create a new branch for development.

```shell
git checkout -b branch-name
```

The name of branch should be semantic, avoiding words like 'update' or 'tmp'. We suggest to use `feature/xxx`, if the modification is about to implement a new feature.

### 4. Make your changes

Now you can create your patch, including appropriate test cases in the new branch.

### 5. Commit your changes

Commit your changes If your changes pass the tests. You are encouraged to use [angular commit-message-format][angular-commit-message-format] to write commit message. In this way, we could have a more trackable history and an automatically generated changelog.

```shell
git add .
git commit -m "fix: add license headers (#264)"
```

### 6. Sync your local repository with the upstream

Keep your local repository updated with upstream repository by:

```shell
git remote add upstream git@github.com:2020NCOV/ncov-report-mini-program-server.git
git fetch upstream master
git rebase upstream/master
```

If conflicts arise, you need to resolve the conflicts manually, then:

```shell
git add my-fix-file
git rebase --continue
```

### 7. Push your branch to GitHub

```shell
git push -f origin branch-name
```

### 8. Create a Pull Request

In GitHub, send a pull request to `2020NCOV:ncov-report-mini-program-server`.

To make sure we can easily recap what happened previously, we have prepared a [pull request template][pr-template] and you need to fill out the PR template.

The core team is monitoring for pull requests. We will review your pull request and either merge it, request changes to it, or close it with an explanation.

If we suggest changes then:

-   Make the required updates.

-   Re-run the test to ensure tests are still passing.

-   Commit your changes with `--amend` and force push to your GitHub repository (this will update your Pull Request):

    ```shell
    git add .
    git commit --amend
    git push -f origin branch-name
    ```

That's it! Thank you for your contribution!

### 9. After your pull request is merged

After your pull request is merged, you can safely delete your branch and pull the changes from the upstream repository:

-   Delete the remote branch on GitHub either through the GitHub web UI or your local shell as follows:

    ```shell
    git push origin --delete branch-name
    ```

-   Check out the master branch:

    ```shell
    git checkout master -f
    ```

-   Delete the local branch:

    ```shell
    git branch -D my-fix-branch
    ```

-   Update your master with the latest upstream version:

    ```shell
    git pull --ff upstream master
    ```

[coc]: ./CODE_OF_CONDUCT.md

[new-issue]: https://github.com/2020NCOV/ncov-report-mini-program-server/issues/new

[issue-label]: https://github.com/2020NCOV/ncov-report-mini-program-server/labels

[good-first-issues]: https://github.com/2020NCOV/ncov-report-mini-program-server/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22+

[repo]: https://github.com/2020NCOV/ncov-report-mini-program-server

[angular-commit-message-format]: https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#-git-commit-guidelines

[pr-template]: ./.github/pull_request_template.md

[issue-template]: ./.github/issue_template.md
