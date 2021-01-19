---
title: Grid Engine
weight: 1
layout: single
publishdate: 2021-01-19 04:00:00 +0000
authors:
  - "Evan Floden"
  - "Alain Coletta"
  - "Seqera Labs"

headline: 'Grid Engine Compute Environment'
description: 'Step-by-step instructions to set up Grid engine for Nextflow Tower.'
menu:
  docs:
    parent: Compute Environments
    weight: 4

---
## Overview

[Grid engine](https://www.univa.com/products/univa-grid-engine.php) is a workload management tool maintained by Altair.

## Requirements

To launch pipelines into a **Grid engine** scheduler from Tower, the following requirements must be fulfilled:

* The cluster should be reachable via an SSH connection using an SSH key.
* The cluster should allow outbound connections to the Tower web service.
* The cluster queue used to run the Nextflow head job must be able to submit cluster jobs.
* The Nextflow runtime version 21.01.1-edge (or later) should be installed on the cluster.


## Compute environment

Follow these steps to create a new compute environment for Grid Engine:

**1.** In the navigation bar on the upper right, choose your account name then choose "Compute environments". Then, click on the **New Environment** button.

{{% pretty_screenshot img="/uploads/2021/01/new_env.png" %}}

<br>

**2.** Enter a descriptive name (e.g. *Grid Engine On-prem*) and select **Grid Engine** as the target platform.

{{% pretty_screenshot img="/uploads/2021/01/grid-engine_new_env.png" %}}

<br>

**3.** Select the **+** sign to add new SSH credentials.

**4.** Enter a name for the credentials

**5.** Enter your **SSH private key** and associated **Passphrase** if required then click **Create**.

{{% pretty_screenshot img="/uploads/2021/01/grid-engine_tower_credentials.png" %}}

{{% tip %}}
A passphrase for your SSH key may be optional depending on how it was created. See [here](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) for detailed instructions for how to create a key.
{{% /tip %}}

<br>

**6.** Enter the absolute path of the **Work directory** to be used on the cluster.

**7.** Enter the absolute path of the **Launch directory** to be used on the cluster.

**8.** Enter the **Login hostname**. This is usually the cluster login node address.

**9.** The **Head queue name** which is the name of the queue, on the cluster, used to launch the execution of the Nextflow runtime.

**10.** The **Compute queue name** which is the name of queue, on the cluster, to which pipeline jobs are submitted.

**11.** Select **Create** to finalize the creation of the compute environment.

{{% pretty_screenshot img="/uploads/2021/01/grid-engine_tower_options.png" %}}

{{% tip %}}
The Compute queue can be overridden as a configuration option in the Nextflow pipeline configuration. See Nextflow [docs](https://www.nextflow.io/docs/latest/process.html#queue) for more details.
{{% /tip %}}

{{% star "Groovy!" %}}
You are now ready to launch pipelines.
{{% /star %}}

Jump to the documentation section for [Launching Pipelines](/docs/launch/overview/).