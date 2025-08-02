# webapp

A Helm chart for deploying webapp

## Get Started

## TL;DR

```bash
helm repo add webapp https://example.com/
helm install webapp/webapp
```

## Introduction

This chart bootstraps a [webapp](https://example.com/) deployment on a [Kubernetes](https://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Prerequisites

- Kubernetes 1.19+
- Helm 3.2.0+

## Installing the Chart

To install the chart with the release name `my-release`:

```bash
helm install my-release webapp/webapp
```

The command lists the resources deployed by the chart.

## Uninstalling the Chart

To uninstall the `my-release` deployment:

```bash
helm uninstall my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration

The following table lists the configurable parameters of the webapp chart and their default values.

| Parameter | Description | Default |
|---|---|---|
| `replicaCount` | Number of webapp replicas | `1` |
| `image.repository` | webapp image repository | `mcr.microsoft.com/dotnet/samples/webapp` |
| `image.tag` | webapp image tag | `latest` |
| `image.pullPolicy` | webapp image pull policy | `IfNotPresent` |
| `service.type` | webapp service type | `ClusterIP` |
| `service.port` | webapp service port | `80` |
|
