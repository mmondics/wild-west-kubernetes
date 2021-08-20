# Building a Multiarchitecture Container Image and Deploying on IBM Z and x86 with Red Hat Advanced Cluster Management

<mark>You can find a video of this demonstration here: <https://youtu.be/zqFAugjXZrA><mark>

## Tools Used

1. Red Hat Advanced Cluster Management (RHACM)
1. OpenShift Container Platform on x86 and IBM Z on-premises
1. GitHub
1. Quay.io Container Registry
1. buildah
1. podman

## Goal of Demonstration

The goal of this demo is to show how easily one can use a Dockerfile to build a multiarchitecture container image that supports IBM Z from a single-architecture container image originally built just for x86. We will then use RHACM to deploy this multiarchitecture container image to multiple OpenShift clusters of different architectures (x86 and IBM Z) at the same time.

## Demo Steps
Add labels to atsocppa and x3wk clusters: demo=multiarch

### Explore RHACM

### Deploy  Initial Application from RHACM
1. Create application.
    * Name: wildwest-multiarch
    * Namespace: wildwest
    * Repository Type: Git
    * URL: <https://github.com/mmondics/wild-west-kubernetes>
    * Deploy application resources only on clusters matching specific labels:
        * Label Name: demo
        * Label Value: multiarch
1. Click Save in the top right of the page

### Investigate Application Error on IBM Z Cluster
Show RHACM overview with errors

### Rebuild Container Image as Multi-Architecture

### Re-deploy Application from RHACM

### Cleanup