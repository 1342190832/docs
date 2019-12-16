---
title: Installing Rancher in an Air Gapped Environment
weight: 2
aliases:
  - /rancher/v2.x/en/installation/air-gap-installation/
  - /rancher/v2.x/en/installation/air-gap-high-availability/
  - /rancher/v2.x/en/installation/air-gap-single-node/
---

This section is about installations of Rancher server in an air gapped environment. An air gapped environment could be where Rancher server will be installed offline, behind a firewall, or behind a proxy. Throughout the installations instructions, there will be _tabs_ for either a high availability installation or a single node installation.

### Air Gapped High Availability (HA) Installations

Rancher recommends installing Rancher in a Highly Available (HA) configuration in an air gapped environment.

An HA installation is comprised of three nodes running the Rancher server components on a Kubernetes cluster. The persistence layer (etcd) is also replicated on these three nodes, providing redundancy and data duplication in case one of the nodes fails.

### Air Gapped Single Node Installations

These instructions also cover how to install Rancher on a single node in an air gapped environment.

The single-node Docker installation is for Rancher users that are wanting to test out Rancher. Instead of running on a Kubernetes cluster, you install the Rancher server component on a single node using a `docker run` command. Since there is only one node and a single Docker container, if the node goes down, there is no copy of the etcd data available on other nodes and you will lose all the data of your Rancher server.

> **Important:** If you install Rancher following the single node installation guide, there is no upgrade path to transition your single node installation to a HA installation.

Instead of running the single node installation, you have the option to follow the HA install guide, but only use one node to install Rancher. Afterwards, you can scale up the etcd nodes in your Kubernetes cluster to make it a HA installation.

# Installation Outline

- [1. Prepare your Node(s)]({{< baseurl >}}/rancher/v2.x/en/installation/other-installation-methods/air-gap/prepare-nodes/)
- [2. Collect and Publish Images to your Private Registry]({{< baseurl >}}/rancher/v2.x/en/installation/other-installation-methods/air-gap/populate-private-registry/)
- [3. Launch a Kubernetes Cluster with RKE]({{< baseurl >}}/rancher/v2.x/en/installation/other-installation-methods/air-gap/launch-kubernetes/)
- [4. Install Rancher]({{< baseurl >}}/rancher/v2.x/en/installation/other-installation-methods/air-gap/install-rancher/)

### [Next: Prepare your Node(s)]({{< baseurl >}}/rancher/v2.x/en/installation/other-installation-methods/air-gap/prepare-nodes/)
