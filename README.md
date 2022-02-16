# docs-csb-gcp

This repo contains the Cloud Service Broker for GCP documentation.

## Branches in this Content Repo

The master branch is the tree-trunk, so **always** make changes you want carried forward in this branch. This includes:

* Unreleased features
* Doc bug fixes
* Doc reorganization or enhancement

Then, if necessary, immediately cherry-pick/copy any changes that you want to push immediately to production into the appropriate branches listed below:

| Branch Name| Use for… |
|------------| ---------|
| master     | 1.n Use for staging doc for the next release. (staged here: TBA)

## Book Repo

The book repo associated with this content is [pivotal-cf/docs-book-csb-gcp](https://github.com/pivotal-cf/docs-book-csb-gcp).

### Staging Environment

TBA

### Making Your Documentation Changes Live

TBA

### Contributing to Documentation

If there is some documentation to add for an unreleased patch version of Cloud Service Broker then create a branch off of the **live** branch
you intend to modify and create a pull request against that branch.
After the version that change is targeting is released, the pull request can be merged and will be live
the next time a documentation deployment occurs.

If the documentation is meant to be target several released versions,
then you will need to:
+ create a pull request for each individual minor version
+ or ask the technical writer to cherry-pick to particular branches/versions.

### Partials

Cross-product partials (if any) for Cloud Service Broker are single sourced from the [Docs Partials](https://github.com/pivotal-cf/docs-partials) repository.

### Releasing a New Minor Version

Because **master** is the latest and greatest documentation, the process would be to cut a **x.x** branch
for the version that **master** was targeting during that time.
A corresponding branch in in the [docs-book-csb-gcp][docs-book-csb-gcp] repository would also need to be made.

After this point, **master** will then be the target for the next version of the Cloud Service Broker product.

## Style Guide

This is a word list for terminology and word usage specific to the Cloud Service Broker for docs.
