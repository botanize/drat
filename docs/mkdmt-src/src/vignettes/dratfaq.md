# Drat Frequently Asked Questions

Dirk Eddelbuettel  
2016-10-27  

## What is drat?

Good question.  Drat is an R package which makes it really easy to provide R
packages via a _repository_, and also makes it easy to use such repositories
for package installation and upgrades.

## Why use drat?

The motivation for drat is to give package authors more control over how they
make their packages available to users. It does this by enabling package
authors to make releases on a GitHub repository (or any server, more on this
below). drat allows anyone to create their own package repository -- just
like [CRAN](https://cran.r-project.org).

There are two key advantages of using drat over other methods of installing
packages from GitHub. First is that a package installed from a drat
repository will be supported by `install.packages()` and `update.packages()`,
so the user has easy methods for keeping up-to-date. A second advantage of
using drat is that the package author can control what other people get when
they download your package from GitHub.  With other methods, users typically
download a random install snapshot, which might have unexpected consequences
for them.

## Where is drat?

drat itself is a package, so it has source code (on GitHub) and a package (on
the main R repository network).

But wait: we also call the repositories created or used via drat "drat"
repositories.  So we have to distinguish between "drat the package" and "a
drat repository" created or used by it.

Hope this clarified things a little. Drat really can be different things
which reside in different places but it aims to be _a helper package which
helps creating and using R package repositories easier_.

## What other documentation is there?

Glad you asked.  We have written

+ a [package webpage](https://dirk.eddelbuettel.com/code/drat.html) giving a
first instroduction
+ several [blog posts](https://dirk.eddelbuettel.com/blog/code/drat/) on the package
and its releases
+ the [GitHub page README](https://github.com/eddelbuettel/drat)
+ several [vignettes accessible from the package page](https://cran.r-project.org/package=drat)
and other places.
+ the [drat repo page](https://eddelbuettel.github.io/drat/)


## Why the focus on GitHub?

Several answers:

+ Because it is there and used by ever increasing numbers of package authors.
+ Because it is pretty fast and reliable, no matter where in the world you are.
+ Because it _already gives every repository owner a web-server_ via either a
gh-pages branch or a `docs/` directory.
+ Because all we need is a web-server and some file system space
+ Because the single variable `user` uniquely identifies a URL
`user.github.io/drat/`, and communicating a single variable is easier than
communicating a full URL

Taken together, we have this a pretty good to _default on GitHub_ for
repositories.  But read on ...

## What if not GitHub?

Fear not, as drat also supports repositories on a local drive, or shared
network drive, or actually just about anything where you can write to or read
from.

We detail that in the corresponding vignettes.

## Why could install_github be wrong?

`install_github()` is a fine tool and does what it sets out to do: grab a
snapshot from GitHub and install it.  This can be the HEAD (by default), or a
tag, or a commit, or from a branch.

But we think that is not what R needs. R has become so very successful for
many reasons, but (in the eyes of many) one key part of the success was
_repositories_ ensuring both _easy installation_ and _easy upgrades_.

That second point is lost on `install_github()`: it installs what we may call
"orphans".  Packages that are disconnected from an upgrade path.  (With the
exception, of course, of a newer version of what you install appearing in a
known repository so that `update.packages` will see it.)  We think that is a
disservice to the users, and a repository can do better in a fundamental way
than provide access to (somewhat random) commits.  Of course, one _could_ write
new code building on top of `install_github()` and adding the functionality.
But then, why? R already has this functionality, and had it for decades:
using repositories.  So drat does not aim to replace `install_github()`; it
simply aims at something both different and possibly much simpler.

Moreover, drat puts the "release" option back into the hand of the _package
authors_. By cutting a release tarball and placing it into a repository, we
think a possibly more informed release snapshot is distributed than by
pointing at any branch of repository.

And last but not least, drat (>= 0.0.4) and its repositories also support binary
installations.

## Can drat work with binaries?

You bet.  Jan Schulz provided a
[careful pull request](https://github.com/eddelbuettel/drat/pull/16) to
provide initial support upon which we have built. As of release 0.1.0,
this should just work for both Windows and OS X.

## Can drat act as an `Additional_repositories` ?

Glad you asked!  In fact, you can use
[this GitHub query](https://github.com/search?q=Additional_repositories+drat&type=Code&utf8=%E2%9C%93)
to find several dozen of packages using `Additional_repositories` to point to
drat repos (still having drat in their name; others may use domain nane
such that the search may miss them). One example we used to point to here
changed however. So for a more stable use case, one example from my packages:
the [RcppRedis package](https://cran.r-project.org/package=RcppRedis) points
[via this line](https://github.com/eddelbuettel/rcppredis/blob/e103ea1cb682ea164bf8a2ae022df64154466e58/DESCRIPTION#L21)
to the [ghrr drat](https://ghrr.github.io/drat/) to (optionally) use the
[RcppMsgPack](https://github.com/eddelbuettel/rcppmsgpack) package (which is
not on CRAN as it uses a MsgPack release newer than what it in Debian).

## What about the miniCRAN package?

The [miniCRAN](https://cran.r-project.org/package=miniCRAN) package creates
self-sufficient repositories by examining the dependency graph and
downloading all dependent packages.  As such, it is more of complement to
drat than an alternative --- and Word is that several people have in fact
combined both.

## Is there a suggested commit message converntion?

The small helper script `getCommitMessageForDrat.sh` implements a simple
format I have suggested in the past and used:

```sh
edd@max:~/git/drat(master)$ inst/scripts/getCommitMessageForDrat.sh 
drat 0.1.0 94248ed git@github.com:eddelbuettel/drat.git
edd@max:~/git/drat(master)$ 
```

It combined four elements:

- the package name
- the current version
- the current git repository commit hash marker
- the repository URL.

When both source and binary packages are uploaded, I often add `(src)` or
`(win)` to indicate the type of package committed.

This format has worked and could form the basis of a standard, but
suggestions and refinements are certainly welcome.
