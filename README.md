# docs-csb-gcp

This repo contains the Cloud Service Broker for GCP documentation.

In this README:

- [Branches in this Content Repo](#branches-in-this-content-repo)
- [Releasing a New Minor Version](#releasing-a-new-minor-version)
- [Partials](#partials)
- [Contributing to Documentation](#contributing-to-documentation)
- [Publishing Docs](#publishing-docs)
- [Troubleshooting Markdown](#troubleshooting-markdown)
- [Style Guide](#style-guide)

## Branches in this Content Repo

The master branch is the tree-trunk, so **always** make changes you want carried forward in this branch. This includes:

* Unreleased features
* Doc bug fixes
* Doc reorganization or enhancement

Then, if necessary, immediately cherry-pick/copy any changes that you want to push immediately to production into the appropriate branches listed below:

| Branch Name | Use for…                                                                                                                                                         |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| main      | Use for staging doc for the next release. (staged here: https://docs-staging.vmware.com/en/draft/Tanzu-Cloud-Service-Broker-for-GCP/1.2/csb-gcp/GUID-index.html) |
| 1.1         | Published at https://docs.vmware.com/en/Tanzu-Cloud-Service-Broker-for-GCP/1.1/csb-gcp/GUID-index.html                                                           |
| 1.0         | Published at https://docs.vmware.com/en/Tanzu-Cloud-Service-Broker-for-GCP/1.0/csb-gcp/GUID-index.html                                                           |
| 0.2         | Published at https://docs.vmware.com/en/Tanzu-Cloud-Service-Broker-for-GCP/0.2/csb-gcp/GUID-index.html                                                           |

## Releasing a New Minor Version

Because **master** is the latest and greatest documentation, the process would be to cut a **x.x** branch
for the version that **master** was targeting during that time.

After this point, **master** will then be the target for the next version of the Cloud Service Broker product.


## Partials

Cross-product partials (if any) for Cloud Service Broker are single sourced from the [Docs Partials](https://github.com/pivotal-cf/docs-partials) repository.


## Contributing to Documentation

If there is some documentation to add for an unreleased patch version of Cloud Service Broker then create a branch off of the **live** branch
you intend to modify and create a pull request against that branch.
After the version that change is targeting is released, the pull request can be merged and will be live
the next time a documentation deployment occurs.

If the documentation is meant to be target several released versions,
then you will need to:
+ create a pull request for each individual minor version
+ or ask the technical writer to cherry-pick to particular branches/versions.

For instructions on how to create a pull request on a branch and instructions on how to create a
pull request using a fork, see
[Creating a PR](https://docs-wiki.sc2-04-pcf1-apps.oc.vmware.com/wiki/external/create-pr.html)
in the documentation team wiki.


## Publishing Docs

- [docworks](https://docworks.vmware.com/) is the main tool for managing docs used by writers.
- [docsdash](https://docsdash.vmware.com/) is a deployment UI which manages the promotion from
staging to pre-prod to production. The process below describes how to upload our docs to staging,
replacing the publication with the same version.

### Prepare Markdown Files
- Markdown files live in this repo.
- Images should live in an `images` directory at the same level and linked with a relative link.
- Each page requires an entry in [config/toc.md](config/toc.md) for the table of contents.
- Variables live in [config/template_variables.yml](config/template_variables.yml).

### In Docsdash

1. Wait about 1 minute for processing to complete after uploading.
2. Go to https://docsdash.vmware.com/deployment-stage

   There should be an entry with a blue link which says `Documentation` and points to staging.

### Promoting to Pre-Prod and Prod

**Prerequisite** Needs additional privileges - reach out to a manager on the docs team [#tanzu-docs](https://vmware.slack.com/archives/C055V2M0H) or ask a writer to do this step for you.

1. Go to Staging publications in docsdash  
  https://docsdash.vmware.com/deployment-stage

2. Select a publication (make sure it's the latest version)

3. Click "Deploy selected to Pre-Prod" and wait for the pop to turn green (refresh if necessary after about 10s)

4. Go to Pre-Prod list  
  https://docsdash.vmware.com/deployment-pre-prod

5. Select a publication

6. Click "Sign off for Release"

7. Wait for your username to show up in the "Signed off by" column

8. Select the publication again

9. Click "Deploy selected to Prod"

## Troubleshooting Markdown

| Problem   | List displays as a paragraph                                                              |
|-----------|-------------------------------------------------------------------------------------------|
| Symptom:  | Bulleted or numbered lists look fine on GitHub but display as a single paragraph in HTML. |
| Solution: | Add a blank line after the stem sentence and before the first item in the list.           |

| Problem   | List numbering is broken: every item is `1.`                            |
|-----------|-------------------------------------------------------------------------|
| Symptom:  | Each numbered item in a list is a `1.` instead of `1.`, `2.`, `3.`, etc |
| Solution: | Try removing any blank newlines within each step.                       |

| Problem   | Code boxes not showing                                                                |
|-----------|---------------------------------------------------------------------------------------|
| Symptom:  | VMware publishing system doesn't accept code tags after the three back ticks.         |
| Solution: | Make sure you're not using `shell` or `bash` or `console` or `yaml` after back ticks. |

## Style Guide

This is a word list for terminology and word usage specific to the Cloud Service Broker for docs.
