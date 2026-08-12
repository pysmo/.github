# Contributing

Thank you for considering contributing! We welcome your contribution. To make
the process as seamless as possible, please read through this guide carefully.

This file is a general guide shared across the projects in the pysmo
organisation. Some repositories also have a more detailed, project-specific
contributing guide in their own documentation — check for a "Development" or
"Contributing" section there first.

## Ways to contribute

There are several ways to contribute, and not all of them involve writing code:

- _Questions_: asking for help when something is unclear or you get stuck is one
    of the easiest ways to contribute. Questions help us identify areas that
    need attention. Development happens publicly on GitHub, so please post
    questions there too — either as a new issue or a discussion. Feel free to
    answer questions from other users as well (including your own, should you
    figure it out!).
- _Bug reports_: if something needs fixing, we want to hear about it! Please
    create a new issue, or add information to an existing one if the bug has
    already been reported. Bonus points if you also provide a patch that fixes
    it!
- _Enhancements_: if you use the project, you can also write code that becomes
    part of it.

If you do want to submit code, please follow the steps outlined below.

## What should be included?

A good contribution contains well-written, documented code along with meaningful
tests to ensure consistent, bug-free behaviour.

## Submitting code

Code submitted via pull request has a much greater chance of being included than
patches sent via email.

The typical workflow is to fork the repository, configure git to sync your fork
with the upstream repository, and then create a feature branch for your changes:

```bash
git checkout -b my_cool_feature
```

Before submitting a pull request from your feature branch, please make sure you
have done the following:

- Write code that adheres to the [PEP 8](https://peps.python.org/pep-0008/)
    style guide.
- Include unit tests with your submission. If you need help with that, feel free
    to contact us.
- Run a code linter and verify that all unit tests pass. The command
    `make tests` should complete without errors.
- To keep a clean git history, please
    [rebase](https://git-scm.com/docs/git-rebase) your feature branch onto the
    upstream `master` branch and squash your commits into a single,
    well-documented commit. This avoids entries like "fix typo" or "undo
    changes" in the git log. Do this before submitting your initial pull request.

Once a pull request is submitted:

- Unit tests run automatically in clean Python environments via GitHub Actions.
    Please verify that all tests pass. If tests pass locally but fail in the
    pull request, you may have forgotten to add a dependency to `pyproject.toml`
    that happened to already be installed on your machine.
- A documentation build is also triggered automatically where applicable. Follow
    the link that appears in the pull request on GitHub and verify the
    documentation looks as expected.
- We will then review your submission and hopefully be able to include it!
