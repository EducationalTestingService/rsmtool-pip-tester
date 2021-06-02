## Introduction

This project is to test the PyPI packages for [RSMTool](https://github.com/EducationalTestingService/rsmtool) on Linux and Windows. We do not test on macOS; we assume that if the package works on Linux, it will also work on macOS.

To test a new package version that has been already built and uploaded to the the Python Package Index, create a new branch, change the `RSMVERSION` values in both `.gitlab-ci.yml` and `azure-pipelines.yml` to the version you want to test, and submit a pull request for the branch. If both builds pass, merge the PR. You can then delete the pull request without merging it.

The packages are tested by creating a new conda environment and installing the specified RSMTool version and its dependencies using `pip`. The code for RSMTool is also checked out in a separate directory and then the tests are run with the installed rsmtool package in the environment.

These builds should only be run right before doing an RSMTool release.
