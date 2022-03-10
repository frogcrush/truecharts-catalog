# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"jetbrains/teamcity-server"` |  |
| image.tag | string | `"2021.2.3@sha256:1cc075a30b3f6ba5a43eec77c2dff1f52db97ecdf7f941b95684e73f066e7f1d"` |  |
| podSecurityContext.runAsGroup | int | `0` |  |
| podSecurityContext.runAsUser | int | `0` |  |
| securityContext.allowPrivilegeEscalation | bool | `true` |  |
| securityContext.readOnlyRootFilesystem | bool | `false` |  |
| securityContext.runAsNonRoot | bool | `false` |  |
| service.main.ports.main.port | int | `9089` |  |
| service.main.ports.main.targetPort | int | `80` |  |

All Rights Reserved - The TrueCharts Project
