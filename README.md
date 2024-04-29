# platform-actions

![Current State](https://img.shields.io/badge/current%20state-volatile-orange)

Github Action workflows for installing and configuring app platform dial-tone


## Table of Contents

* [Prerequisites](#prerequisites)
* [Getting Started](#getting-started)
* [Usage](#usage)


## Prerequisites

### Account credentials

* [Github](https://github.com/)
* One or more on: [AWS](https://aws.amazon.com/), [Azure](https://azure.microsoft.com/en-us/), [Google Cloud](https://cloud.google.com/), [Oracle](https://www.oracle.com/cloud/)
* [Tanzu Network](https://network.pivotal.io)

### CLIs

* [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [gh](https://github.com/cli/cli#installation)


## Getting started

Start by [forking this Github repository](https://docs.github.com/en/get-started/quickstart/fork-a-repo#forking-a-repository).  You're required to [configure your own set of Github secrets](https://github.com/Azure/actions-workflow-samples/blob/master/assets/create-secrets-for-GitHub-workflows.md) that will be leveraged by a collection of [Github Actions](.github/workflows).

If you're looking to contribute, clone your fork to your local workstation or laptop, [create a branch](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging) and get to work on that new feature.  This repo is open for [pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).


To keep your fork up-to-date with upstream changes

```bash
git remote add upstream https://github.com/clicktruck/platform-actions
```
> Execute once


```bash
#! with git CLI
git fetch upstream
git merge upstream/main
git push

#! alternatively with gh CLI
gh repo sync --source clicktruck/platform-actions
```
> Execute periodically

## Usage

Review this curated collection of dispatch workflows.

| Action | Link |
| :---   | :---: |
| Clean Workflow Logs | [:white_check_mark:](../../actions/workflows/clean-workflow-run-logs.yml) |
| Relocate images from Tanzu Network to private container image registry | [:white_check_mark:](../../actions/workflows/relocate-tap-images-from-tanzu-network-to-container-registry-dispatch.yml) |
| Install Tanzu Cluster Essentials | [:white_check_mark:](../../actions/workflows/install-tanzu-cluster-essentials-dispatch.yml) |
| Install Tanzu Data Services Repository | [:white_check_mark:](../../actions/workflows/install-tanzu-data-services-repo-dispatch.yml) |
| Install Ingress Providers (contour, cert-manager, external-dns) | [:white_check_mark:](../../actions/workflows/install-tanzu-ingress-dispatch.yml) |
| Install Tanzu Standard Repository | [:white_check_mark:](../../actions/workflows/install-tanzu-standard-repo-dispatch.yml) |
| Create new project in Harbor | [:white_check_mark:](../../actions/workflows/create-harbor-project-dispatch.yml) |
| _Install Tanzu Application Platform_ |   |
| » Single cluster | [:construction:](../../actions/workflows/install-tanzu-application-platform-dispatch.yml) |
| » Multi cluster (targeting: AWS) | [:construction:](../../actions/workflows/multi-cluster-tanzu-application-platform-install-on-aws-dispatch.yml) |
| » Multi cluster (targeting: Azure) | [:construction:](../../actions/workflows/multi-cluster-tanzu-application-platform-install-on-azure-dispatch.yml) |
| » Multi cluster (targeting: Google Cloud) | [:construction:](../../actions/workflows/multi-cluster-tanzu-application-platform-install-on-google-dispatch.yml) |
| Onboard cluster to Application Live View | [:construction:](../../actions/workflows/onboard-cluster-to-app-live-view-dispatch.yml) |
| Prepare Metadata Secrets Store | [:construction:](../../actions/workflows/prepare-metadata-store-secrets-dispatch.yml) |
| _Uninstall Tanzu Application Platform_ |   |
| » Single cluster | [:construction:](../../actions/workflows/uninstall-tanzu-application-platform-dispatch.yml) |
| Uninstall Tanzu Data Services Repository | [:white_check_mark:](../../actions/workflows/uninstall-tanzu-data-services-repo-dispatch.yml) |
| Uninstall Ingress Providers (contour, cert-manager, external-dns) | [:white_check_mark:](../../actions/workflows/uninstall-tanzu-ingress-dispatch.yml) |
| Uninstall Tanzu Standard Repository | [:white_check_mark:](../../actions/workflows/uninstall-tanzu-standard-repo-dispatch) |