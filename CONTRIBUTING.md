# Contributors Guide

Thank you for considering contributing to the maintenance or development of
Stack, or otherwise supporting users of Stack! We hope that the following
information will encourage and assist you. We start with some advice about
Stack's goals and governance, and approach to supporting users.

## Stack's goals

Stack's current goals are:

* To provide easy to use tooling for Haskell development
* To provide complete support for at least the following three development
  environments: Linux, macOS, and Windows
* To address the needs of industrial users, open source maintainers, and other
  people
* To focus on the 'curated package set' use case
* To prioritize reproducible build plans

The goals above are not set in stone. However, any major changes to them
should involve significant public discussion and a public vote by the Stack
maintainer team.

## Stack's governance

People involved in maintaining or developing Stack with rights to make commits
to the repository can be classified into two groups: 'committers' and
'maintainers'.

### Stack's committers

We encourages a wide range of people to be granted rights to make commits to the
repository.

People are encouraged to take initiative to make non-controversial
changes, such as documentation improvements, bug fixes, performance
improvements, and feature enhancements.

Maintainers should be included in discussions of controversial changes and
tricky code changes.

Our general approach is **"it's easier to ask forgiveness than permission"**. If
there is ever a bad change, it can always be rolled back.

### Stack's maintainers

Stack's maintainers are long-term contributors to the project. Michael Snoyman
(@snoyberg) was the founder of Stack, and its initial maintainer - and he has
added others. Michael's current interests and priorities mean that he is no
longer actively involved in adding new features to Stack.

Maintainers are recognized for their contributions including:

* Direct code contribution
* Review of pull requests
* Interactions on the GitHub issue tracker
* Documentation management
* External support - for example, hosting or training

The maintainer team make certain decisions when that is necessary, specifically:

* How to proceed, if there is disagreement on how to do so on a specific topic
* Whether to add or remove (see further below) a maintainer

Generally, maintainers are only removed due to non-participation or actions
unhealthy to the project. Removal due to non-participation is not a punishment,
simply a recognition that maintainership is for active participants only.

We hope that removal due to unhealthy actions will never be necessary, but would
include protection for cases of:

* Disruptive behavior in public channels related to Stack
* Impairing the codebase through bad commits/merges

Like committers, maintainers are broadly encouraged to make autonomous
decisions. Each maintainer is empowered to make a unilateral decision. However,
maintainers should favor getting consensus first if:

* They are uncertain what is the best course of action
* They anticipate that other maintainers or users of Stack will disagree on the
  decision

## Stack's support

A large part of the general discussion around Stack is on support-related
topics, and that is reflected in the current issue tracker content. Assistance
in responding to such matters is greatly appreciated.

While support-related matters can be posted here as an 'issue', we encourage the
use of other forums, in particular
[Haskell's Discourse](https://discourse.haskell.org/). We also recommend
Haskell's Discourse for general discussions about Stack's current or desired
features. Stack is also discussed on Reddit's
[Haskell community](https://www.reddit.com/r/haskell/).

We encourage use of those other forums because support-related discussions can
clog up the issue tracker and make it more difficult to maintain the project.
People needing support may also get a faster and fuller response on other
forums.

Additions to the issue tracker are better suited to concrete feature proposals,
bug reports, and other code base discussions (for example, refactorings).

## Bug Reports

Please [open an issue](https://github.com/commercialhaskell/stack/issues/new)
and use the provided template to include all necessary details.

The more detailed your report, the faster it can be resolved and will ensure it
is resolved in the right way. Once your bug has been resolved, the responsible
person will tag the issue as _Needs confirmation_ and assign the issue back to
you. Once you have tested and confirmed that the issue is resolved, close the
issue. If you are not a member of the project, you will be asked for
confirmation and we will close it.

## Documentation

The files which make up Stack's documentation are located in the `doc`
directory of the repository. They are formatted in the
[Markdown syntax](https://daringfireball.net/projects/markdown/), with some
extensions.

Those files are rendered on [haskellstack.org](http://haskellstack.org) by
[Read the Docs](https://readthedocs.org/) using
[MkDocs](https://www.mkdocs.org/) and the
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme. The
`stable` branch of the repository provides the 'stable' version of the online
documentation. The `master` branch provides the 'latest' version of the
documentation.

The 'stable' version of the online documentation is intended to be applicable to
the latest released version of Stack. If you would like to help with that
documentation, please submit a
[pull request](https://help.github.com/articles/using-pull-requests/) with your
changes/additions based off the
[stable branch](https://github.com/commercialhaskell/stack/tree/stable).

The specific versions of the online documentation (eg `v: v2.7.5`) are generated
from the content of files at the point in the repository's history specified
by the corresponding release tag. Consequently, that content is fixed once
released.

The Markdown syntax supported by MkDocs and the Material for MkDocs theme can
differ from the GitHub Flavored Markdown ([GFM](https://github.github.com/gfm/))
supported for content on GitHub.com. Please refer to the
[MkDocs documentation](https://www.mkdocs.org/user-guide/writing-your-docs/#writing-with-markdown)
and the
[Material for MkDocs reference](https://squidfunk.github.io/mkdocs-material/reference/)
to ensure your pull request will achieve the desired rendering.

The configuration file for MkDocs is `mkdocs.yml`. The extensions to the basic
Markdown syntax used include:

* admonitions
* code blocks, with syntax highlighting provided by
  [Pygments](https://pygments.org/)
* content tabs, which can be nested
* icons and emojis

The files in the `doc` directory of the repository include two symbolic links
(symlinks), `ChangeLog.md` and `CONTRIBUTING.md`. Users of Git on Windows should
be aware of its approach to symbolic links. See the
[Git for Windows Wiki](https://github.com/git-for-windows/git/wiki/Symbolic-Links).
If `git config --show-scope --show-origin core.symlinks` is `false` in a local
repository on Windows, then the files will be checked out as small plain files
that contain the link text  See the
[Git documentation](https://git-scm.com/docs/git-config#Documentation/git-config.txt-coresymlinks).

## Code

If you would like to contribute code to fix a bug, add a new feature, or
otherwise improve `stack`, pull requests are most welcome. It's a good idea to
[submit an issue](https://github.com/commercialhaskell/stack/issues/new) to
discuss the change before plowing into writing code.

If you'd like to help out but aren't sure what to work on, look for issues with
the
[awaiting pull request](https://github.com/commercialhaskell/stack/issues?q=is%3Aopen+is%3Aissue+label%3A%22awaiting+pull+request%22)
label. Issues that are suitable for newcomers to the codebase have the
[newcomer friendly](https://github.com/commercialhaskell/stack/issues?q=is%3Aopen+is%3Aissue+label%3A%22awaiting+pull+request%22+label%3a%22newcomer+friendly%22)
label. Best to post a comment to the issue before you start work, in case anyone
has already started.

Please include a
[ChangeLog](https://github.com/commercialhaskell/stack/blob/master/ChangeLog.md)
entry and
[documentation](https://github.com/commercialhaskell/stack/tree/master/doc/)
updates with your pull request.

## Backwards Compatability

The `stack` executable does not need to, and does not, strive for the same broad
compatability with versions of GHC that a library package (such as `pantry`)
would seek. Instead, the `stack` executable aims to define a well-known
combination of dependencies on which it relies. That is applies in particular to
the `Cabal` package, where the `stack` executable aims to support one, and only
one, version of `Cabal` with each release of the executable. At the time of
writing (April 2022) that combination is defined by resolver `lts-17.5` (for
GHC 8.10.4, and including `Cabal-3.2.1.0`) - see `stack.yaml`.

## Code Quality

The Stack project uses [yamllint](https://github.com/adrienverge/yamllint) as a
YAML file quality tool and [HLint](https://github.com/ndmitchell/hlint) as a
code quality tool.

### Linting of YAML files

The yamllint configuration extends the tools default and is set out in
`.yamllint.yaml`. In particular, indentation is set at 2 spaces and `- ` in
sequences is treated as part of the indentation.

### Linting of Haskell source code

The HLint configurations is set out in `.hlint.yaml`.

Stack contributors need not follow dogmatically the suggested HLint hints but
are encouraged to debate their usefulness. If you find a HLint hint is not
useful and detracts from readability of code, consider marking it in the
[configuration file](https://github.com/commercialhaskell/stack/blob/master/.hlint.yaml)
to be ignored. Please refer to the
[HLint manual](https://github.com/ndmitchell/hlint#readme)
for configuration syntax.

Quoting
[@mgsloan](https://github.com/commercialhaskell/stack/pulls?utf8=%E2%9C%93&q=is%3Apr%20author%3Amgsloan):

> We are optimizing for code clarity, not code concision or what HLint thinks.

You can install HLint with Stack. You might want to install it in the global
project in case you run into dependency conflicts. HLint can report hints in
your favourite text editor. Refer to the HLint repository for more details.

To install, command:

~~~text
stack install hlint
~~~

Once installed, you can check your changes with command:

~~~text
stack exec -- sh ./etc/scripts/hlint.sh
~~~

## Testing

The Stack code has both unit tests and integration tests. Integration tests can
be found in the
[test/integration](https://github.com/commercialhaskell/stack/tree/master/test/integration)
folder and unit tests, in the
[src/test](https://github.com/commercialhaskell/stack/tree/master/src/test)
folder. Tests are written using the [Hspec](https://hspec.github.io/) framework.
In order to run the full test suite, you can simply command:

~~~text
stack test
~~~

The `--file-watch` is a very useful option to get quick feedback. However,
running the entire test suite after each file change will slow you down. You'll
need to specify which test suite (unit test or integration) and pass arguments
to specify which module you'd specifically like to run to get quick feedback. A
description of this follows below.

### Working with Unit Tests

If you would like to run the unit tests on their own, you can command:

~~~text
stack test stack:stack-test
~~~

Running an individual module works with a command like this:

~~~text
stack test stack:stack-test --ta "-m <PATTERN>"
~~~

Where `<PATTERN>` is the name of the module without `Spec.hs`.

You may also load tests into GHCi and run them with these command:

~~~text
stack ghci stack:stack-test --only-main
# GHCi starting up output ...
> :main -m "<PATTERN>"
~~~

Where again, `<PATTERN>` is the name of the module without `Spec.hs`.

### Working with Integration Tests

Running the integration tests is a little involved, you'll need to command:

~~~text
stack build --flag stack:integration-tests stack --exec stack-integration-test
~~~

Running an individual module works with a command like this:

~~~text
stack build --flag stack:integration-tests stack --exec "stack-integration-test -m <PATTERN>"
~~~

Where `<PATTERN>` is the name of the folder listed in the
[test/integration/tests/](https://github.com/commercialhaskell/stack/tree/master/test/integration/tests)
directory.

You may also achieve this through GHCi with this command:

~~~text
stack ghci stack:stack-integration-test
# GHCi starting up output ...
> :main -m "<PATTERN>"
~~~

Where again, `<PATTERN>` is the name of the folder listed in the
[test/integration/tests/](https://github.com/commercialhaskell/stack/tree/master/test/integration/tests)
directory.

## Continuous integration (CI)

We use [GitHub Actions](https://docs.github.com/en/actions) to do CI on Stack.
The configuration of the workflows is in the YAML files in `.github/workflows`.
The current active workflows are:

### Linting - `lint.yml`

This workflow will run if:
* there is a pull request
* commits are pushed to these branches: `master`, `stable` and `rc/**`

The workflow has one job (`style`). It runs on `ubuntu` only and applies
yamllint and Hlint.

### Test suite - `unit-tests.yml`

This workflow will run if:
* there is a pull request
* commits are pushed to these branches: `master`, `stable` and `rc/**`.
* requested

The workflow has two jobs: `pedantic` and `unit-tests`.

The `pedantic` job runs on `ubuntu` only and builds Stack with the
`--pedantic` flag.

The `unit-tests` job runs on a matrix of operating systems and Stack
project-level YAML configuration files (`stack.yaml`). It builds and tests Stack
with the following flags: `--haddock --no-haddock-deps`.

Its approach to creating a cache depends on the operating system. Its 'Cache
dependencies on Unix-like OS' step caches the Stack root on Unix-like operating
systems. Its 'Cache dependencies on Windows' step caches the same information
on Windows, but takes into account that a relevant directory is located outside
of the Stack root.

### Integration-based - `integration-tests.yml`

This workflow will run if:
* there is a pull request
* commits are pushed to these branches: `master`, `stable` and `rc/**`
* any tag is created
* requested

The workflow has three jobs: `integration-tests`, `linux-arm64` and
`github-release`.

The `integration-tests` job runs on a matrix of operating systems (`ubuntu`,
`windows` and `macos`) and makes use of the `release.hs` script at
`etc/scripts`. Its approach to creating a cache is the same as for
`unit-tests.yml`, described above.

Its 'Install deps and run checks' step uses `release.hs check`.

Its 'Build bindist' step uses `release.hs build`.

Its 'Upload bindist' step uploads artifacts using the name of the runner's
operating system (`Linux`, `Windows` or `macOS`) as the name for the artifacts.

The `linux-arm64` job runs on a self-hosted runner for Linux and ARM64. It makes
use of Docker and a Docker file at `etc/dockerfiles/arm64.Dockerfile`.

Its 'Build bindist' step makes use of a compiled version of `release.hs` script
at `etc/scripts` to command `release build`.

Its 'Upload bindist' step uploads artifacts using `Linux-ARM64` as the name for
the artifacts.

The `github-release` job needs `integration-tests` and `linux-arm64`. It only
takes effect if the trigger for the workflow was the creation of a tag.

Its four steps `Download Linux/Windows/macOS/Linux-ARM64 artifact` download the
named artifacts to path `_release`.

Its step 'Hash and sign assets' makes use of a 'secret' environment variable
`RELEASE_SIGNING_KEY` established by the owner of the Stack repository. The
variable contains the private key for the GPG key with ID 0x575159689BEFB442.
That key is imported into GPG and then used by GPG to create a detached signature
for each file.

### Inactive - `stan.yml`

Stan is a Haskell static analysis tool. As of 29 August 2022, it does not
support GHC >= 9.0.1 and Stack is built with GHC >= 9.2.4. Consequently, this
workflow does not run. Its intent is to apply Stan to Stack.

## Slack channel

If you're making deep changes and real-time communication with the Stack team
would be helpful, we have a `#stack-collaborators` Slack channel in the
Haskell Foundation workspace. To join the workspace, follow this
[link](https://haskell-foundation.slack.com/join/shared_invite/zt-z45o9x38-8L55P27r12YO0YeEufcO2w#/shared-invite/email).
