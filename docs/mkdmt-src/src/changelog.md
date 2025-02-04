###  2022 

2022-04-13  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): Release 0.2.3 
 
2022-04-06  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): Roll minor version 
 
        * tests/testArmBinary.R: New test for binaries on Arm 
 
2022-04-05  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): Roll minor version 
 
        * inst/extdata/4.1/arm64/foo_1.3.tgz: Added new test package 
        * inst/extdata/big-sur-arm64/bin/4.1/bat_1.3.tgz: Idem 
        * inst/extdata/src/foo_1.3.tar.gz: Idem 
        * inst/extdata/src/bar_1.0.tar.gz: Idem 
 
        * tests/skeleton_git2r.R: Adjusting to new test packages 
 
###  2021 

2021-12-02  Dirk Eddelbuettel  <edd@debian.org> 
 
        * docs/mkdmt-src/src/vignettes/dratforusers.md: Also fix typo here 
 
2021-12-02  Noam Ross <noam.ross@gmail.com> 
 
        * vignettes/DratForPackageUsers.md: Fix one-char typo (from 2015 !!) 
 
2021-12-01  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): Release 0.2.2 
 
2021-11-28  Dirk Eddelbuettel  <edd@debian.org> 
 
         * DESCRIPTION (Version, Date): Roll minor version 
 
        * DESCRIPTION (VignetteBuilder): Converted to simplermarkdown engine 
        * vignettes/*md: Idem 
        * vignettes/*html: Updated 
        * vignettes/water.css: Added 
        * vignettes/Makefile.hidden: Updated, and renamed 
 
2021-11-05  Dirk Eddelbuettel  <edd@debian.org> 
 
         * README.md: Remove Travis badge 
        * .travis.yml: Remove Travis YAML config 
 
2021-07-09  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): Release 0.2.1 
 
        * R/initRepo.R (initRepo): Create a placeholder index.html file in 
        the top-level directory to appease CRAN check of URL 
 
         * R/insertPackage.R (insertPackage): Show a message if no top-level 
        file index.html is found in the given repo directory. 
 
        * vignettes/DratStepByStep.Rmd: Mention that a placeholder index.html 
        file is now installed. 
 
2021-04-29  Dirk Eddelbuettel  <edd@debian.org> 
 
         * DESCRIPTION (Version, Date): Roll minor version 
 
        * R/insertPackage.R (getPackageInfo,identifyPackageType): Mark two 
        functions as internal as they are not exported via NAMESPACE 
        * man/getPackageInfo.Rd: Idem 
        * man/identifyPackageType.Rd: Idem 
 
2021-04-21  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): Release 0.2.0 
 
        * DESCRIPTION (Suggests): Add rmarkdown as required by knitr change 
 
        * inst/NEWS.Rd: Update NEWS.Rd 
 
        * tests/version.R: Add test to ensure NEWS file is current 
 
2021-04-11  Dirk Eddelbuettel  <edd@debian.org> 
 
        * vignettes/DratStepByStep.Rmd: Remove 'draft' from date filed 
 
2021-04-10  Dirk Eddelbuettel  <edd@debian.org> 
 
         * DESCRIPTION (Version, Date): Roll minor version 
 
        * vignettes/CombiningDratAndTravis.Rmd: Use to minidown and water 
        * vignettes/DratFAQ.Rmd: Idem 
        * vignettes/DratForPackageAuthors.Rmd: Idem 
         * vignettes/DratForPackageUsers.Rmd: Idem 
        * vignettes/WhyDrat.Rmd: Idem 
        * DESCRIPTION (Suggests): Add minidown (which implies rmarkdown) 
 
        * DESCRIPTION (Depends): Increase to R (>= 3.6) 
 
        * README.md: Sanitize some links for r-devel link checker 
        * man/drat-package.Rd: Idem 
        * vignettes/DratFAQ.Rmd: Idem 
        * vignettes/DratForPackageAuthors.Rmd: Idem 
        * vignettes/DratStepByStep.Rmd: Idem 
        * vignettes/WhyDrat.Rmd: Idem 
 
2021-04-08  Dirk Eddelbuettel  <edd@debian.org> 
 
        * vignettes/DratStepByStep.Rmd: Fix more typos thanks to Roman 
 
2021-04-08  Felix Ernst  <felix.gm.ernst@outlook.com> 
 
        tests/skeleton_git2r.R: Refactored and restructed for docs/ use 
        R/insertPackage.R: Add error message if DESCRIPTION not found 
 
2021-04-07  Dirk Eddelbuettel  <edd@debian.org> 
 
        * vignettes/DratStepByStep.Rmd: Add new 'step-by-step' vignette 
        written with Roman Hornung 
 
2021-03-29  Dirk Eddelbuettel  <edd@debian.org> 
 
        * vignettes/CombiningDratAndTravis.Rmd: Note on docs/, https:// use 
        * vignettes/DratFAQ.Rmd: Ditto 
        * vignettes/DratForPackageAuthors.Rmd: Ditto 
        * vignettes/DratForPackageUsers.Rmd: Ditto 
        * vignettes/WhyDrat.Rmd: Ditto 
 
2021-03-28  Dirk Eddelbuettel  <edd@debian.org> 
 
        * tests/skeleton_git2r.R (testRepoActions): More work supporting 
        new (optional) docs/ location 
 
        * docs/mkdmt-src/: Moved mkdocs-material input 
 
2021-03-23  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (URL): Add link to repo 
 
2021-03-14  Dirk Eddelbuettel  <edd@debian.org> 
 
        * README.md: Mention drat-base/drat for easier forking 
 
        * R/archivePackages.R (.check_location_arg): Add helper function 
        * R/initRepo.R (initRepo): Use helper function 
        * R/insertPackage.R (insertPackage): Ditto 
        * R/pruneRepo.R (getRepoInfo): Ditto, use option location 
 
2021-03-13  Dirk Eddelbuettel  <edd@debian.org> 
 
         * DESCRIPTION (Version, Date): Roll minor version 
 
        * R/initRepo.R (initRepo): New option location to allow use of docs/ 
        directory instead of gh-pages branch 
        * R/insertPackage.R (insertPackage): Ditto 
        * man/initRepo.Rd: Documentation for new location option 
        * man/insertPackage.Rd: Ditto 
 
2021-02-24  Dirk Eddelbuettel  <edd@debian.org> 
 
        * docs-src/mkdocs.yml: No longer show vignette overview 
 
###  2020 

2020-12-26  Dirk Eddelbuettel  <edd@debian.org> 
 
        * .github/workflows/ci.yaml: Add CI runner using r-ci 
        * README.md: Add new CI badge 
 
2020-09-13  Dirk Eddelbuettel  <edd@debian.org> 
 
        * docs/: Added package website 
        * docs-src/: Added package website inputs 
 
        * README.md: Added badge and short sentence linking to documentation 
 
2020-07-18  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version): Release 0.1.8 
 
2020-07-17  Felix Ernst  <felix.gm.ernst@outlook.com> 
 
        * tests/skeleton_get2r.R: Fixed issue for pruning on r-oldrel 
 
2020-07-10  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version): Release 0.1.7 
 
        * tests/skeleton_git2r.R (testRepoActions): More explicit 
        conditioning on presence of optional git2r 
 
2020-07-05  Felix Ernst  <felix.gm.ernst@outlook.com> 
 
        * man/insertPackages.Rd: document optional arguments more clearly 
        * man/pruneRepo.Rd: document optional arguments more clearly 
        * R/insertPackages.R: minor refactoring 
        * R/pruneRepo.R: minor refactoring 
 
2020-07-02  Dirk Eddelbuettel  <edd@debian.org> 
 
         * DESCRIPTION (Version, Date): Roll minor version 
 
2020-07-01  Felix Ernst  <felix.gm.ernst@outlook.com> 
 
        * R/archivePackages.R: Cover special case of adding to archive 
        * R/pruneRepo.R: Idem 
        * tests/skeleton_get2r.R: Idem 
 
2020-06-30  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): Roll minor version 
 
2020-06-20  Felix Ernst  <felix.gm.ernst@outlook.com> 
 
        * R/pruneRepo.R: New function updateRepo, minor refactoring 
        * R/insertPackages.R: Idem 
        * R/archivePackages.R: Idem 
        * man/pruneRepo.Rd: Document updateRepo 
        * NAMESPACE: Add updateRepo 
 
2020-06-10  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): Roll minor version 
 
        * drat.Rproj: Undo accidental delete in preceding commit storms 
 
2020-06-09  Felix Ernst  <felix.gm.ernst@outlook.com> 
 
        * R/insertPackages.R: Updates to insertPackages function 
        * man/insertPackages.Rd: Idem 
        * R/archivePackages.R: Bug fixes 
        * R/prunePackages.R: Idem 
 
        * tests/skeleton_git2r.R: Added tests for insertPackages, 
        archivePackages and pruneRepo 
        * inst/extdata/*: Added toy packages to support tests 
 
2020-06-08  Felix Ernst  <felix.gm.ernst@outlook.com> 
 
        * R/archivePackages.R: Refactored vectorisation 
        * R/prunePackages.R: Idem 
        * man/addRepo.Rd: Updated 
        * man/archivePackages.Rd: Idem 
        * man/pruneRepo.Rd: Idem 
        * R/insertPackages.R: Added insertPackages function 
        * man/insertPackages.Rd: Idem 
 
2020-06-07  Dirk Eddelbuettel  <edd@debian.org> 
 
        * man/addRepo.Rd: Updated 
        * man/archivePackages.Rd: Idem 
        * man/insertPackages.Rd: Idem 
        * man/pruneRepo.Rd: Idem 
 
2020-06-05  Patrick Schratz  <patrick.schratz@gmail.com> 
 
        * R/archivePackages.R: First pass at vectorising operations 
        * R/insertPackages.R: Idem 
        * R/prunePackages.R: Idem 
        * NAMESPACE: Idem 
 
2020-05-29  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version): Release 0.1.6 
        * README.md: Add Felix Ernst to Authors 
 
2020-05-29  Felix Ernst  <felix.gm.ernst@outlook.com> 
 
        * R/archivePackages.R: Updated mac binary format support 
        * R/insertPackages.R: Idem 
        * R/pruneRepo.R: Idem 
        * man/*: Updated documentation 
        * DESCRIPTION: Roll minor version 
 
2020-05-25  Dirk Eddelbuettel  <edd@debian.org> 
 
        * README.md: Add 'last commit' badge 
 
        * .travis.yml: Switch to bionic and R 4.0.0 
 
2020-04-23  Thomas P. Fuller  <thomas.fuller@coherentlogic.com> 
 
        * README.md: Add entry for thospfuller/drat 
 
###  2019 

2019-03-28  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): Release 0.1.5 
 
        * README.md: Mention Christoph in Author section 
 
        * NAMESPACE: Also import contrib.url() from utils 
 
2019-03-27  Christoph Stepper <christoph.stepper@gfk.com> 
 
        * R/archivePackages.R: Simplification of argument use 
        * R/pruneRepo.R: Idem 
        * R/insertPackage.R: Idem 
        * man/archivePackages.Rd: Idem 
        * man/pruneRepo.Rd: Idem 
 
2019-03-25  Christoph Stepper <christoph.stepper@gfk.com> 
 
        * R/archivePackages.R: Support binary packages 
        * R/pruneRepo.R: Idem 
 
        * man/archivePackages.Rd: Added documentation 
        * man/pruneRepo.Rd: Idem 
 
        * man/*.Rd: Rebuilt under current roxygen2 
 
2019-03-23  Dirk Eddelbuettel  <edd@debian.org> 
 
        * README.md: Add dependencies badge 
 
        * tests/skeleton_git2r.R (testSkeletonGit2r): Ensure 'R' is prefixed 
        by proper path as recommended in Section 1.6 of Writing R Extensions 
 
###  2018 

2018-03-12  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/addRepo.R: Minor documentation update 
        * man/addRepo.Rd: Idem 
 
2018-01-30  Neal Fultz  <nfultz@gmail.com> 
 
        * R/insertPackage.R: Correct working directoru for git2r 
        * tests/skeleton_git2r.R: Add end-to-end test 
 
###  2017 

2017-12-16  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): Release 0.1.4 
 
2017-12-15  Neal Fultz  <nfultz@gmail.com> 
 
        * R/insertPackage.R: Split macOS binaries along R version into 
        mavericks and el-capitan repos; allow for global option() value 
        dratBranch to select a branch to commit to 
 
2017-10-07  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insertPackage.R (insertPackage): Always add PACKAGES.rds 
 
2017-09-16  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): Release 0.1.3 
 
        * R/insertPackage.R (insertPackage): Consider PACKAGES.rds too 
 
        * README.md: Remove one now-defunct drat repo from list 
 
2017-02-23  Dirk Eddelbuettel  <edd@debian.org> 
 
        * .travis.yml (before_install): Use https to fetch script 
 
###  2016 

2016-10-28  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): Release 0.1.2 
 
        * vignettes/DratFAQ.Rmd (vignette): Added 'Why use drat' section 
        at the top based on a suggestion by Ben Marwick 
 
2016-10-24  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): Roll minor version and date 
 
        * README.md: More canonical URLs, and omegahat.net correction 
 
        * vignettes/DratFAQ.Rmd (vignette): More canonical URLs 
        * vignettes/DratForPackageAuthors.Rmd (drat): Ditto 
 
2016-08-14  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Suggests): Add rmarkdown 
 
2016-08-13  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/pruneRepo.R: Extend documentation to also mention option 
        remove="git" to invoke git2r::rm (where available) 
 
2016-08-07  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION: Release 0.1.1 
 
        * DESCRIPTION: Add URL and BugReports links 
 
        * inst/NEWS.Rd: Added 
 
        * README.md: Use canonical CRAN URL 
        * vignettes/DratFAQ.Rmd: Ditto 
 
        * vignettes/DratFAQ.Rmd: Update question on Additional_repositories 
        as the original example moved on 
 
2016-08-01  Dirk Eddelbuettel  <edd@debian.org> 
 
        * .travis.yml: Switch to using run.sh for Travis CI 
 
2016-07-31  Jan Gorecki  <j.gorecki@wit.edu.pl> 
 
        * R/insertPackage.R: Support additional fields 
        * man/insertPackage.Rd: Idem 
 
2016-06-02  Colin Gillespie  <csgillespie@gmail.com> 
 
        * R/addRepo: Use https URLs 
 
2016-03-09  Antonio Piccolboni  <antonio@piccolboni.info> 
 
        * R/pruneRepo.R: Generalize regexp to allow dots in package names 
 
2016-02-28  Dirk Eddelbuettel  <edd@debian.org> 
 
        * vignettes/DratForPackageAuthors.Rmd: Correct file:// URL 
        * vignettes/DratForPackageUsers.Rmd: Idem 
 
2016-02-27  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION: Add versioned Depends: on R (>= 3.2.0) 
 
2016-02-26  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insertPackage.R (insertPackage): Use dir.exists() for directory 
        test (with thanks to Kevin Wright) 
 
###  2015 

2015-08-08  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): New release 0.1.0 
 
        * vignettes/DratFAQ.Rmd (vignette): Updated with respect to support 
        for binary packages on OS X and Windows; added commit message entry 
 
        * inst/scripts/getCommitMessageForDrat.sh: Added 
 
        * README.md: Updated 
 
2015-08-03  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insertPackage.R (getPathForPackage): In case of non-compiled OS X 
        package, issue a message that it will be install in Mavericks path. 
 
2015-08-02  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insertPackage.R (getPackageInfo): New function, building on 
        earlier code by Matt Jones and Jan Schulz 
        (getPathForPackage): Simplified earlier function by Jan and Dirk 
        (insertPackage): Use new / modified functions 
 
        * NAMESPACE: Import two functions from utils to please R CMD check 
        * vignettes/DratForPackageAuthors.Rmd (drat): Use canonical CRAN URL 
        to please R CMD check even more 
 
2015-07-30  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Author): Finally credit all contributors; 
        (Version): Roll minor version 
        (Date): Update Date 
 
2015-07-29  Matt Jones <gitcode@magisa.org> 
 
        * R/insertPackage.R: Better support for OS X binaries via 
        getPathForMac() function which  untars the tgz file, extracts the 
        Built: line from the description, and determines if the build 
        platform was "darwin13", in which case "mavericks" is included on the 
        returned path. 
 
2015-07-25  Thomas Leeper <thosjleeper@gmail.com> 
 
        * R/archivePackages.R: New function to (optionally) archive 
        existing packages when a new one gets added. 
        * R/insertPackages.R: Support archivePackages() 
        * R/pruneRepo.R: Support archivePackages() 
 
2015-06-04  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insertPackage.R (insertPackage): Correct use from .Call to call. 
        with a big Doh! and thanks to Guy Dawson for PR #25 
 
2015-05-26  Dirk Eddelbuettel  <edd@debian.org> 
 
        * vignettes/DratFAQ.Rmd (vignette): Add a short paragraph about miniCRAN 
 
2015-05-25  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): New release 0.0.4 
 
        * README.md: Corrected one URL, added link to drat FAQ 
 
2015-05-24  Dirk Eddelbuettel  <edd@debian.org> 
 
        * vignettes/DratFAQ.Rmd (vignette): Added new section 
 
2015-05-23  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/addRepo.R: In non-GH mode, explicitly check for spaces in the URL 
        and abort if found as file-based access with spaces breaks. 
 
        * R/addRepo.R: State that file-based URL has to be 'file:/some/path' 
        * man/addRepo.Rd: Ditto 
 
2015-05-12  Dirk Eddelbuettel  <edd@debian.org> 
 
        * vignettes/DratFAQ.Rmd (vignette): Small edits 
 
2015-05-10  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION: Roll Date and Version 
 
        * NAMESPACE: Also export new functions pruneRepo and initRepo 
 
        * R/pruneRepo.R (pruneRepo): Added (untested so far) removal 
        * man/pruneRepo.Rd: Initial documentation 
 
        * R/initRepo.R (initRepo): (Very) initial  version of a repo creator 
        * man/initRepo.Rd: Initial documentation 
 
        * R/insertPackage.R (identifyPackageType): Fix documentation typo 
 
2015-04-28  Carl Boettiger <cboettig@gmail.com> 
 
        * R/insertPackage.R (insertPackage): Protect git2r::commit() call 
        with tryCatch() to gracefully deal with error conditions 
 
2015-04-27  Dirk Eddelbuettel  <edd@debian.org> 
 
        * vignettes/DratFAQ.Rmd: Beginnings of a Drat FAQ vignette 
 
2015-04-26  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insertPackage.R (insertPackage): Some tweaking 
 
2015-04-26  Jan Schulz <jasc@gmx.net> 
 
        * R/insertPackage.R (insertPackage): Support Windows and Mac OS X 
        binary packages 
 
2015-04-10  Dirk Eddelbuettel  <edd@debian.org> 
 
        * vignettes/rmd2html.r: Added to process vignettes 
        * vignettes/*.Rmd: Correct VignetteIndexEntry 
        * vignettes/*.html: Added html versions prior to build 
 
2015-04-09  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): New release 0.0.3 
 
        * vignettes/DratForPackageUsers.Rmd: Added new vignette detailing 
        drat use for package users (ie someone installing from a drat) 
 
2015-04-08  Dirk Eddelbuettel  <edd@debian.org> 
 
        * vignettes/DratForPackageAuthors.Rmd: Added new vignette detailing 
        drat use for package authors (ie someone writing to a drat) 
 
2015-03-28  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION: Added knitr to Suggests: and VignetteBuilder: 
        * .travis.yml: Added knitr 
 
2015-03-27  Dirk Eddelbuettel  <edd@debian.org> 
 
        * vignettes/WhyDrat.Rmd: Adding post by Steven as vignette 
 
        * vignettes/CombiningDratAndTravis.Rmd: Adding (work-in-progress) 
        post by Colin 
 
2015-03-26  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/addRepo.R: Added/extended/clarified example 
        * man/addRepo.Rd: Corresponding Rd file 
 
2015-03-22  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insertPackage.R: Support setting a commit message 
 
        * inst/scripts/git2targz.sh: Beginnings of helper script to create a 
        tarball (suitable for a drat repo) given a repo URL 
 
2015-03-16  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insertPackage.R (insertPackage): Use on.exit() with setwd() to 
        ensure we return to current working directory           (closes #9) 
 
2015-03-14  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/addRepo.R: Added examples (inside \dontrun{}) to help page 
 
        * R/insertPackage.R: Idem 
 
2015-03-12  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insertPackage.R (insertPackage): Add quietly=TRUE to 
        requireNamespace 
 
2015-03-04  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insertPackage.R (insertPackage): Correction to file operations 
        and path settings (cf GH issue #7) 
 
2015-03-04  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insertPackage.R (insertPackage): Re-enable git2r::checkout() 
 
2015-02-28  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version, Date): New release 0.0.2 
 
        * R/insertPackage.R: Document git2r in help page, don't use git2r for 
        checkout yet though (cf git2r issue #109) 
 
        * R/pruneRepo.R: Default path for repo also contains src/contrib/; 
        generalize regular expression for source tarball 
 
        * inst/TODO.md: Updated with recent changes 
 
2015-02-27  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insertPackage.R: Use git2r if available 
        * DESCRIPTION: Add Suggests: on git2r 
 
        * DESCRIPTION (Version,Date): Bump Date: and Version: 
 
        * .travis.yml: Also install git2r 
 
2015-02-21  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version,Date): Bump Date: and Version: 
 
        * R/insertPackage.R (insertPackage): Correct directory location for 
        the (optional) git commands 
 
2015-02-10  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/pruneRepo.R (.pruneRepo): Beginnings of a helper function to 
        identify older versions of given packages in a repo directory 
 
        * inst/TODO.md: Added item to generalize sources beyond .tar.gz 
 
2015-02-07  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Version): Bumping Version and Date 
 
2015-02-06  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION (Description): Remove continuation lines which trigger 
        a bug in devtools (cf issue tick #1) 
 
        * man/drat-package.Rd (Maintainer): Correction from pull request #2 
        by Colin Gillespie applied 
 
        * R/addRepo.R: Clarify alturl argument as per issue ticket #3 
        * man/addRepo.Rd: Ditto 
 
2015-02-04  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION: Version 0.0.1 
 
        * DESCRIPTION (Description): And another editing of Description: 
 
2015-02-02  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/addRepo.R (addRepo): Use http, not https, at GitHub 
 
        * man/drat-package.Rd: Ditto 
 
2015-02-01  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insertPackage.R (insertPackage): Renamed from insertRelesae() 
 
        * NAMESPACE: Explicitly expotr addRepo() and insertPackage() 
 
        * R/addRepo.R (add): Also provide unexported alias drat:::add() 
        * R/insertPackage.R (insert): Ditto for drat:::insert() 
 
        * inst/TODO.md: Moved from top-level 
 
        * tests/simpleTests.R (testInsertLocal): Expanded tests 
 
        * .travis.yml (script): Added Travis CI support 
        * .Rbuildignore: Added to exclude Travis file 
 
2015-01-30  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/addRepo.R (addRepo): Renamed from add.R; function now addRepo() 
 
        * R/insertRelease.R (insertRelease): Renamed from insert.R, function 
        renamed too to stress that repos contains releases not commits 
 
        * tests/simpleTests.R: Changed to use addRepo() 
 
2015-01-29  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insert.R (insert): Small enhancements / corrections 
 
2015-01-28  Dirk Eddelbuettel  <edd@debian.org> 
 
        * R/insert.R (insert): Offer optional git add, commit push 
 
        * R/add.R (add): Allow for multiple accounts added at once 
 
        * tests/simpleTests.R: Added first simple test script 
 
        * man/drat-package.Rd: Updated 
 
2015-01-23  Dirk Eddelbuettel  <edd@debian.org> 
 
        * DESCRIPTION: Beginnings of what will become version 0.0.1 
 
        * R/add.R: Initial version 
        * R/insert.R: Ditto 
 
        * TODO.md: Added with some first notes 
