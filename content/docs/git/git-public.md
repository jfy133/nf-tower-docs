---
title: Public git repositories
aliases:
- "/docs/git-public"
weight: 1
layout: single
publishdate: 2020-10-20 04:00:00 +0000
authors:
  - "Evan Floden"
  - "Alain Coletta"
  - "Seqera Labs"
headline: "Public git repositories"
description: 'Managing and connecting to Nextflow workflows in Public git repositories'

menu:
  docs:
    parent: Git Integration
    weight: 2
---
Nextflow data pipelines can pulled remotely from either public or private Git-hosting solutions including the popular platforms: GitHub, GitLab, BitBucket and Gitea.

Launching a publicly hosted git pipelines simply requires adding the git repo URL in the **pipeline to launch** field. 

{{% pretty_screenshot img="/uploads/2020/10/git_public_repo.png" %}}

Note the revision and version numbers for a given repository are automatically pulled using the Git API. By default, the default `main/master` branch will be executed.

{{% tip %}}
[nf-core](https://nf-co.re/pipelines) are a great resource for public nextflow pipelines.
{{% /tip %}}