# Cerebro

Cerebro is an open source (MIT License) elasticsearch web admin tool built using Scala, Play Framework, AngularJS and Bootstrap.

## Introduction

This chart deploys Cerebro to your cluster.
Optionally you can use cerebro provided auth by uploading a Secret with the needed env vars (don't forget to set `AUTH_TYPE`).

## Prerequisites

- Kubernetes 1.9+

## Installing the Chart

Please refer to https://artifacthub.io/packages/helm/labmonkeys-charts/cerebro?modal=install.
You can use the `-f values.yaml` argument to customize the installation to your needs.
The chart is installed by default in the `default` namespace.
Please refer to values.yaml or [Artifact Hub UI](https://artifacthub.io/packages/helm/labmonkeys-charts/cerebro?modal=values-schema) to see parameters and their default values.

## Uninstalling the Chart

To uninstall/delete the `my-cerebro` deployment:

```bash
$ helm delete my-cerebro
```
The command removes all the Kubernetes components associated with the chart and deletes the release.

## Backend connection with basic auth

You can create your secret, make sure the key name is "application.conf" and simply give the secret name `configFromSecretRef:`
