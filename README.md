# appofapps

![Version: 0.0.2](https://img.shields.io/badge/Version-0.0.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.0.1](https://img.shields.io/badge/AppVersion-0.0.1-informational?style=flat-square)

a Helm chart that follows the app of apps pattern.
It is used as a simple mechanism to implement a progressive deployment.

Documentation generated with [helm-docs](https://github.com/norwoodj/helm-docs).

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| clusters | object | `{}` | (map) Target clusters |
| projectName | string | `"default"` | (string) Name of the destination project in ArgoCD |
| remoteChart.name | string | `nil` | Chart name to deploy in the remote clusters |
| remoteChart.namespace | string | `"default"` | (string) Target namespace for the Chart to be applied to |
| remoteChart.repo | string | `nil` | Repository where the Chart can be found |
| remoteChart.revision | string | `nil` | Chart revision |
| remoteChart.values | object | `{}` | (object) Values to pass on to the chart on the remote clusters |
| sequential | bool | `true` | (bool) if `true`, the clusters will be rolled out one after the other, otherwise they will be deployed in parallel |
| syncPolicy.prune | bool | `true` | (bool) Automatically prune resources |
| syncPolicy.selfHeal | bool | `true` | (bool) Automatically heal drifted resources |
