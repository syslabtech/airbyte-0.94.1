# airbyte

![Version: 0.67.17](https://img.shields.io/badge/Version-0.67.17-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: dev](https://img.shields.io/badge/AppVersion-dev-informational?style=flat-square)

Helm chart to deploy airbyte

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://airbytehq.github.io/helm-charts/ | airbyte-api-server | 0.67.17 |
| https://airbytehq.github.io/helm-charts/ | airbyte-bootloader | 0.67.17 |
| https://airbytehq.github.io/helm-charts/ | connector-builder-server | 0.67.17 |
| https://airbytehq.github.io/helm-charts/ | cron | 0.67.17 |
| https://airbytehq.github.io/helm-charts/ | keycloak | 0.67.17 |
| https://airbytehq.github.io/helm-charts/ | keycloak-setup | 0.67.17 |
| https://airbytehq.github.io/helm-charts/ | metrics | 0.67.17 |
| https://airbytehq.github.io/helm-charts/ | pod-sweeper | 0.67.17 |
| https://airbytehq.github.io/helm-charts/ | server | 0.67.17 |
| https://airbytehq.github.io/helm-charts/ | temporal | 0.67.17 |
| https://airbytehq.github.io/helm-charts/ | webapp | 0.67.17 |
| https://airbytehq.github.io/helm-charts/ | worker | 0.67.17 |
| https://airbytehq.github.io/helm-charts/ | workload-api-server | 0.67.17 |
| https://airbytehq.github.io/helm-charts/ | workload-launcher | 0.67.17 |
| https://charts.bitnami.com/bitnami | common | 1.x.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| airbyte-api-server.affinity | object | `{}` | Affinity and anti-affinity for webapp pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| airbyte-api-server.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| airbyte-api-server.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| airbyte-api-server.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| airbyte-api-server.containerSecurityContext.runAsGroup | int | `1000` |  |
| airbyte-api-server.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| airbyte-api-server.containerSecurityContext.runAsUser | int | `1000` |  |
| airbyte-api-server.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| airbyte-api-server.enabled | bool | `true` |  |
| airbyte-api-server.env_vars | object | `{}` |  |
| airbyte-api-server.image.pullPolicy | string | `"IfNotPresent"` | The pull policy to use for the airbyte airbyte-api-server image |
| airbyte-api-server.image.repository | string | `"airbyte/airbyte-api-server"` | The repository to use for the airbyte airbyte-api-server image. |
| airbyte-api-server.ingress.annotations | object | `{}` | Ingress annotations done as key:value pairs |
| airbyte-api-server.ingress.className | string | `""` | Specifies ingressClassName for clusters >= 1.18+ |
| airbyte-api-server.ingress.enabled | bool | `false` | Set to true to enable ingress record generation |
| airbyte-api-server.ingress.hosts | list | `[]` | The list of hostnames to be covered with this ingress record. |
| airbyte-api-server.ingress.tls | list | `[]` | Custom ingress TLS configuration |
| airbyte-api-server.livenessProbe.enabled | bool | `true` | Enable livenessProbe on the server |
| airbyte-api-server.livenessProbe.failureThreshold | int | `3` | Failure threshold for livenessProbe |
| airbyte-api-server.livenessProbe.initialDelaySeconds | int | `30` | Initial delay seconds for livenessProbe |
| airbyte-api-server.livenessProbe.periodSeconds | int | `10` | Period seconds for livenessProbe |
| airbyte-api-server.livenessProbe.successThreshold | int | `1` | Success threshold for livenessProbe |
| airbyte-api-server.livenessProbe.timeoutSeconds | int | `10` | Timeout seconds for livenessProbe |
| airbyte-api-server.log.level | string | `"INFO"` | The log level to log at. |
| airbyte-api-server.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| airbyte-api-server.podSecurityContext | object | `{"fsGroup":1000}` | Security context for the container |
| airbyte-api-server.readinessProbe.enabled | bool | `true` | Enable readinessProbe on the server |
| airbyte-api-server.readinessProbe.failureThreshold | int | `3` | Failure threshold for readinessProbe |
| airbyte-api-server.readinessProbe.initialDelaySeconds | int | `10` | Initial delay seconds for readinessProbe |
| airbyte-api-server.readinessProbe.periodSeconds | int | `10` | Period seconds for readinessProbe |
| airbyte-api-server.readinessProbe.successThreshold | int | `1` | Success threshold for readinessProbe |
| airbyte-api-server.readinessProbe.timeoutSeconds | int | `10` | Timeout seconds for readinessProbe |
| airbyte-api-server.replicaCount | int | `1` | Number of airbyte-api-server replicas |
| airbyte-api-server.resources.limits | object | `{}` | The resources limits for the airbyte-api-server container |
| airbyte-api-server.resources.requests | object | `{}` |  |
| airbyte-api-server.service.port | int | `80` |  |
| airbyte-api-server.tolerations | list | `[]` | Tolerations for webapp pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| airbyte-bootloader.affinity | object | `{}` | Affinity and anti-affinity for bootloader pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| airbyte-bootloader.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| airbyte-bootloader.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| airbyte-bootloader.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| airbyte-bootloader.containerSecurityContext.runAsGroup | int | `1000` |  |
| airbyte-bootloader.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| airbyte-bootloader.containerSecurityContext.runAsUser | int | `1000` |  |
| airbyte-bootloader.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| airbyte-bootloader.enabled | bool | `true` |  |
| airbyte-bootloader.env_vars | object | `{}` | Supply extra env variables to main container using simplified notation |
| airbyte-bootloader.extraContainers | list | `[]` | Additional container for server pod(s) |
| airbyte-bootloader.extraEnv | list | `[]` | Supply extra env variables to main container using full notation |
| airbyte-bootloader.extraInitContainers | list | `[]` | Additional init containers for server pods |
| airbyte-bootloader.extraVolumeMounts | list | `[]` | Additional volumeMounts for server containers |
| airbyte-bootloader.extraVolumes | list | `[]` | Additional volumes for server pods |
| airbyte-bootloader.image.pullPolicy | string | `"IfNotPresent"` | The pull policy to use for the airbyte bootloader image |
| airbyte-bootloader.image.repository | string | `"airbyte/bootloader"` | The repository to use for the airbyte bootloader image. |
| airbyte-bootloader.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| airbyte-bootloader.podAnnotations | object | `{}` | Add extra annotations to the bootloader pod |
| airbyte-bootloader.podLabels | object | `{}` | Add extra labels to the bootloader pod |
| airbyte-bootloader.podSecurityContext | object | `{"fsGroup":1000}` | Security context for the container |
| airbyte-bootloader.resources.limits | object | `{}` | The resources limits for the airbyte bootloader image |
| airbyte-bootloader.resources.requests | object | `{}` | The requested resources for the airbyte bootloader image |
| airbyte-bootloader.secrets | object | `{}` | Supply additional secrets to container |
| airbyte-bootloader.tolerations | list | `[]` | Tolerations for worker pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| connector-builder-server.affinity | object | `{}` | Affinity and anti-affinity for webapp pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| connector-builder-server.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| connector-builder-server.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| connector-builder-server.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| connector-builder-server.containerSecurityContext.runAsGroup | int | `1000` |  |
| connector-builder-server.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| connector-builder-server.containerSecurityContext.runAsUser | int | `1000` |  |
| connector-builder-server.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| connector-builder-server.enabled | bool | `true` |  |
| connector-builder-server.env_vars | object | `{}` |  |
| connector-builder-server.image.pullPolicy | string | `"IfNotPresent"` | The pull policy to use for the airbyte connector-builder-server image |
| connector-builder-server.image.repository | string | `"airbyte/connector-builder-server"` | The repository to use for the airbyte connector-builder-server image. |
| connector-builder-server.livenessProbe.enabled | bool | `true` | Enable livenessProbe on the server |
| connector-builder-server.livenessProbe.failureThreshold | int | `3` | Failure threshold for livenessProbe |
| connector-builder-server.livenessProbe.initialDelaySeconds | int | `30` | Initial delay seconds for livenessProbe |
| connector-builder-server.livenessProbe.periodSeconds | int | `10` | Period seconds for livenessProbe |
| connector-builder-server.livenessProbe.successThreshold | int | `1` | Success threshold for livenessProbe |
| connector-builder-server.livenessProbe.timeoutSeconds | int | `10` | Timeout seconds for livenessProbe |
| connector-builder-server.log.level | string | `"INFO"` | The log level to log at. |
| connector-builder-server.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| connector-builder-server.podSecurityContext | object | `{"fsGroup":1000}` | Security context for the container |
| connector-builder-server.readinessProbe.enabled | bool | `true` | Enable readinessProbe on the server |
| connector-builder-server.readinessProbe.failureThreshold | int | `3` | Failure threshold for readinessProbe |
| connector-builder-server.readinessProbe.initialDelaySeconds | int | `10` | Initial delay seconds for readinessProbe |
| connector-builder-server.readinessProbe.periodSeconds | int | `10` | Period seconds for readinessProbe |
| connector-builder-server.readinessProbe.successThreshold | int | `1` | Success threshold for readinessProbe |
| connector-builder-server.readinessProbe.timeoutSeconds | int | `10` | Timeout seconds for readinessProbe |
| connector-builder-server.replicaCount | int | `1` | Number of connector-builder-server replicas |
| connector-builder-server.resources.limits | object | `{}` | The resources limits for the connector-builder-server container |
| connector-builder-server.resources.requests | object | `{}` | The requested resources for the connector-builder-server container |
| connector-builder-server.service.port | int | `80` |  |
| connector-builder-server.tolerations | list | `[]` | Tolerations for webapp pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| cron.affinity | object | `{}` | Affinity and anti-affinity for cron pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| cron.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| cron.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| cron.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| cron.containerSecurityContext.runAsGroup | int | `1000` |  |
| cron.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| cron.containerSecurityContext.runAsUser | int | `1000` |  |
| cron.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| cron.enabled | bool | `true` |  |
| cron.env_vars | object | `{}` | Supply extra env variables to main container using simplified notation |
| cron.extraContainers | list | `[]` | Additional container for cron pods |
| cron.extraEnv | list | `[]` | Supply extra env variables to main container using full notation |
| cron.extraInitContainers | list | `[]` | Additional init containers for cron pods |
| cron.extraVolumeMounts | list | `[]` | Additional volumeMounts for cron containers |
| cron.extraVolumes | list | `[]` | Additional volumes for cron pods |
| cron.image.pullPolicy | string | `"IfNotPresent"` | The pull policy to use for the airbyte cron image |
| cron.image.repository | string | `"airbyte/cron"` | The repository to use for the airbyte cron image. |
| cron.livenessProbe.enabled | bool | `true` | Enable livenessProbe on the cron |
| cron.livenessProbe.failureThreshold | int | `3` | Failure threshold for livenessProbe |
| cron.livenessProbe.initialDelaySeconds | int | `30` | Initial delay seconds for livenessProbe |
| cron.livenessProbe.periodSeconds | int | `10` | Period seconds for livenessProbe |
| cron.livenessProbe.successThreshold | int | `1` | Success threshold for livenessProbe |
| cron.livenessProbe.timeoutSeconds | int | `1` | Timeout seconds for livenessProbe |
| cron.log.level | string | `"INFO"` | The log level to log at. |
| cron.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| cron.podAnnotations | object | `{}` | Add extra annotations to the cron pods |
| cron.podLabels | object | `{}` | Add extra labels to the cron pods |
| cron.podSecurityContext | object | `{"fsGroup":1000}` | Security context for the container |
| cron.readinessProbe.enabled | bool | `true` | Enable readinessProbe on the cron |
| cron.readinessProbe.failureThreshold | int | `3` | Failure threshold for readinessProbe |
| cron.readinessProbe.initialDelaySeconds | int | `10` | Initial delay seconds for readinessProbe |
| cron.readinessProbe.periodSeconds | int | `10` | Period seconds for readinessProbe |
| cron.readinessProbe.successThreshold | int | `1` | Success threshold for readinessProbe |
| cron.readinessProbe.timeoutSeconds | int | `1` | Timeout seconds for readinessProbe |
| cron.replicaCount | int | `1` | Number of cron replicas |
| cron.resources.limits | object | `{}` | The resources limits for the cron container |
| cron.resources.requests | object | `{}` | The requested resources for the cron container |
| cron.secrets | object | `{}` | Supply additional secrets to container |
| cron.tolerations | list | `[]` | Tolerations for cron pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| externalDatabase.database | string | `""` | Database name |
| externalDatabase.existingSecret | string | `""` | Name of an existing secret resource containing the DB password |
| externalDatabase.existingSecretPasswordKey | string | `""` | Name of an existing secret key containing the DB password |
| externalDatabase.host | string | `""` | Database host |
| externalDatabase.jdbcUrl | string | `""` | Database full JDBL URL (ex: jdbc:postgresql://host:port/db?parameters) |
| externalDatabase.password | string | `""` | Database password |
| externalDatabase.port | string | `""` | Database port number |
| externalDatabase.user | string | `""` | non-root Username for Airbyte Database |
| fullnameOverride | string | `""` | String to fully override airbyte.fullname template with a string |
| global.airbyteUrl | string | `""` | The URL where Airbyte will be reached; This should match your Ingress host |
| global.airbyteYml | string | `""` |  |
| global.auth | object | `{"instanceAdmin":{"emailSecretKey":"instance-admin-email","firstName":"","lastName":"","passwordSecretKey":"instance-admin-password","secretName":"airbyte-config-secrets"}}` | Auth configuration |
| global.auth.instanceAdmin | object | `{"emailSecretKey":"instance-admin-email","firstName":"","lastName":"","passwordSecretKey":"instance-admin-password","secretName":"airbyte-config-secrets"}` | Admin user configuration |
| global.auth.instanceAdmin.emailSecretKey | string | `"instance-admin-email"` | The key within `emailSecretName` where the initial user's email is stored |
| global.auth.instanceAdmin.firstName | string | `""` | The first name of the initial user |
| global.auth.instanceAdmin.lastName | string | `""` | The last name of the initial user |
| global.auth.instanceAdmin.passwordSecretKey | string | `"instance-admin-password"` | The key within `passwordSecretName` where the initial user's password is stored |
| global.auth.instanceAdmin.secretName | string | `"airbyte-config-secrets"` | Secret name where the instanceAdmin configuration is stored |
| global.database | object | `{"database":"","host":"","password":"","port":"","secretName":"","type":"internal","user":""}` | Database configuration |
| global.database.database | string | `""` | The database name |
| global.database.host | string | `""` | The database host |
| global.database.password | string | `""` | The database password |
| global.database.port | string | `""` | The database port |
| global.database.secretName | string | `""` | Secret name where database credentials are stored |
| global.database.user | string | `""` | The database user |
| global.deploymentMode | string | `"oss"` | Deployment mode, whether or not render the default env vars and volumes in deployment spec |
| global.edition | string | `"community"` | Edition; "community" or "pro" |
| global.enterprise.licenseKeySecretKey | string | `"license-key"` | The key within `licenseKeySecretName` where the Airbyte license key is stored |
| global.enterprise.secretName | string | `"airbyte-config-secrets"` | Secret name where an Airbyte license key is stored |
| global.env_vars | object | `{}` | Environment variables |
| global.jobs.kube.annotations | object | `{}` | key/value annotations applied to kube jobs |
| global.jobs.kube.images.busybox | string | `""` | busybox image used by the job pod |
| global.jobs.kube.images.curl | string | `""` | curl image used by the job pod |
| global.jobs.kube.images.socat | string | `""` | socat image used by the job pod |
| global.jobs.kube.labels | object | `{}` | key/value labels applied to kube jobs |
| global.jobs.kube.main_container_image_pull_secret | string | `""` | image pull secret to use for job pod |
| global.jobs.kube.nodeSelector | object | `{}` | Node labels for pod assignment |
| global.jobs.kube.tolerations | list | `[]` | Node tolerations for pod assignment  Any boolean values should be quoted to ensure the value is passed through as a string. |
| global.jobs.resources.limits | object | `{}` | Job resource limits |
| global.jobs.resources.requests | object | `{}` | Job resource requests |
| global.metrics.metricClient | string | `""` | The metric client to configure globally. Supports "otel" |
| global.metrics.otelCollectorEndpoint | string | `""` | The open-telemetry-collector endpoint that metrics will be sent to |
| global.serviceAccountName | string | `"airbyte-admin"` | Service Account name override |
| global.storage.type | string | `"minio"` |  |
| keycloak-setup.affinity | object | `{}` | Affinity and anti-affinity for webapp pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| keycloak-setup.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| keycloak-setup.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| keycloak-setup.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| keycloak-setup.containerSecurityContext.runAsGroup | int | `1000` |  |
| keycloak-setup.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| keycloak-setup.containerSecurityContext.runAsUser | int | `1000` |  |
| keycloak-setup.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| keycloak-setup.enabled | bool | `true` |  |
| keycloak-setup.env_vars | object | `{}` |  |
| keycloak-setup.initContainerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| keycloak-setup.initContainerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| keycloak-setup.initContainerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| keycloak-setup.initContainerSecurityContext.runAsGroup | int | `101` |  |
| keycloak-setup.initContainerSecurityContext.runAsNonRoot | bool | `true` |  |
| keycloak-setup.initContainerSecurityContext.runAsUser | int | `100` |  |
| keycloak-setup.initContainerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| keycloak-setup.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| keycloak-setup.podSecurityContext | object | `{"fsGroup":1000}` | Security context for the container |
| keycloak-setup.tolerations | list | `[]` | Tolerations for webapp pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| keycloak.affinity | object | `{}` | Affinity and anti-affinity for webapp pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| keycloak.auth.adminPassword | string | `"keycloak123"` |  |
| keycloak.auth.adminUsername | string | `"airbyteAdmin"` |  |
| keycloak.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| keycloak.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| keycloak.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| keycloak.containerSecurityContext.runAsGroup | int | `0` |  |
| keycloak.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| keycloak.containerSecurityContext.runAsUser | int | `1000` |  |
| keycloak.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| keycloak.enabled | bool | `true` |  |
| keycloak.env_vars | object | `{}` |  |
| keycloak.initContainerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| keycloak.initContainerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| keycloak.initContainerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| keycloak.initContainerSecurityContext.runAsGroup | int | `70` |  |
| keycloak.initContainerSecurityContext.runAsNonRoot | bool | `true` |  |
| keycloak.initContainerSecurityContext.runAsUser | int | `70` |  |
| keycloak.initContainerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| keycloak.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| keycloak.podSecurityContext | object | `{"fsGroup":0}` | Security context for the container |
| keycloak.tolerations | list | `[]` | Tolerations for webapp pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| metrics.affinity | object | `{}` | Affinity and anti-affinity for metrics-reporter pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| metrics.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| metrics.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| metrics.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| metrics.containerSecurityContext.runAsGroup | int | `1000` |  |
| metrics.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| metrics.containerSecurityContext.runAsUser | int | `1000` |  |
| metrics.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| metrics.enabled | bool | `false` |  |
| metrics.env_vars | object | `{}` |  |
| metrics.extraContainers | list | `[]` |  |
| metrics.extraEnv | list | `[]` | Additional env vars for metrics-reporter pods |
| metrics.extraVolumeMounts | list | `[]` | Additional volumeMounts for metrics-reporter containers |
| metrics.extraVolumes | list | `[]` | Additional volumes for metrics-reporter pods |
| metrics.image.pullPolicy | string | `"IfNotPresent"` | The pull policy to use for the airbyte metrics-reporter image |
| metrics.image.repository | string | `"airbyte/metrics-reporter"` | The repository to use for the airbyte metrics-reporter image. |
| metrics.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| metrics.podAnnotations | object | `{}` | Add extra annotations to the metrics-reporter pod |
| metrics.podLabels | object | `{}` | Add extra labels to the metrics-reporter pod |
| metrics.podSecurityContext | object | `{"fsGroup":1000}` | Security context for the container |
| metrics.replicaCount | int | `1` | Number of metrics-reporter replicas |
| metrics.resources.limits | object | `{}` | The resources limits for the metrics-reporter container |
| metrics.resources.requests | object | `{}` | The requested resources for the metrics-reporter container |
| metrics.secrets | object | `{}` |  |
| metrics.tolerations | list | `[]` | Tolerations for metrics-reporter pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| minio.affinity | object | `{}` | Affinity and anti-affinity for minio pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| minio.image.repository | string | `"minio/minio"` | Minio image used by Minio helm chart |
| minio.image.tag | string | `"RELEASE.2023-11-20T22-40-07Z"` | Minio tag image |
| minio.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ # |
| minio.storage.volumeClaimValue | string | `"500Mi"` |  |
| minio.tolerations | list | `[]` | Tolerations for minio pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ # |
| nameOverride | string | `""` | String to partially override airbyte.fullname template with a string (will prepend the release name) |
| pod-sweeper.affinity | object | `{}` | Affinity and anti-affinity for pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| pod-sweeper.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| pod-sweeper.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| pod-sweeper.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| pod-sweeper.containerSecurityContext.runAsGroup | int | `1001` |  |
| pod-sweeper.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| pod-sweeper.containerSecurityContext.runAsUser | int | `1001` |  |
| pod-sweeper.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| pod-sweeper.enabled | bool | `true` |  |
| pod-sweeper.extraVolumeMounts | list | `[]` | Additional volumeMounts for podSweeper container(s). |
| pod-sweeper.extraVolumes | list | `[]` | Additional volumes for podSweeper pod(s). |
| pod-sweeper.image.pullPolicy | string | `"IfNotPresent"` | The pull policy for the pod sweeper image |
| pod-sweeper.image.repository | string | `"bitnami/kubectl"` | The image repository to use for the pod sweeper |
| pod-sweeper.image.tag | string | `"1.28.9"` | The pod sweeper image tag to use |
| pod-sweeper.livenessProbe.enabled | bool | `true` | Enable livenessProbe on the podSweeper |
| pod-sweeper.livenessProbe.failureThreshold | int | `3` | Failure threshold for livenessProbe |
| pod-sweeper.livenessProbe.initialDelaySeconds | int | `5` | Initial delay seconds for livenessProbe |
| pod-sweeper.livenessProbe.periodSeconds | int | `30` | Period seconds for livenessProbe |
| pod-sweeper.livenessProbe.successThreshold | int | `1` | Success threshold for livenessProbe |
| pod-sweeper.livenessProbe.timeoutSeconds | int | `1` | Timeout seconds for livenessProbe |
| pod-sweeper.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| pod-sweeper.podAnnotations | object | `{}` | Add extra annotations to the podSweeper pod |
| pod-sweeper.podLabels | object | `{}` | Add extra labels to the podSweeper pod |
| pod-sweeper.podSecurityContext | object | `{"fsGroup":1001}` | Security context for the container |
| pod-sweeper.readinessProbe.enabled | bool | `true` | Enable readinessProbe on the podSweeper |
| pod-sweeper.readinessProbe.failureThreshold | int | `3` | Failure threshold for readinessProbe |
| pod-sweeper.readinessProbe.initialDelaySeconds | int | `5` | Initial delay seconds for readinessProbe |
| pod-sweeper.readinessProbe.periodSeconds | int | `30` | Period seconds for readinessProbe |
| pod-sweeper.readinessProbe.successThreshold | int | `1` | Success threshold for readinessProbe |
| pod-sweeper.readinessProbe.timeoutSeconds | int | `1` | Timeout seconds for readinessProbe |
| pod-sweeper.resources.limits | object | `{}` | The resources limits for the podSweeper container |
| pod-sweeper.resources.requests | object | `{}` | The requested resources for the podSweeper container |
| pod-sweeper.tolerations | list | `[]` | Tolerations for pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| postgresql.affinity | object | `{}` | Affinity and anti-affinity for postgresql pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| postgresql.commonAnnotations."helm.sh/hook" | string | `"pre-install"` | It will determine when the hook should be rendered |
| postgresql.commonAnnotations."helm.sh/hook-weight" | string | `"-1"` | The order in which the hooks are executed. If weight is lower, it has higher priority |
| postgresql.containerSecurityContext.allowPrivilegeEscalation | bool | `false` | Ensures the container will run with a non-root user |
| postgresql.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| postgresql.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| postgresql.containerSecurityContext.runAsGroup | int | `70` |  |
| postgresql.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| postgresql.containerSecurityContext.runAsUser | int | `70` |  |
| postgresql.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| postgresql.enabled | bool | `true` | Switch to enable or disable the PostgreSQL helm chart |
| postgresql.existingSecret | string | `""` | Name of an existing secret containing the PostgreSQL password ('postgresql-password' key) |
| postgresql.image.repository | string | `"airbyte/db"` |  |
| postgresql.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| postgresql.podSecurityContext.fsGroup | int | `70` |  |
| postgresql.postgresqlDatabase | string | `"db-airbyte"` | Airbyte Postgresql database |
| postgresql.postgresqlPassword | string | `"airbyte"` | Airbyte Postgresql password |
| postgresql.postgresqlUsername | string | `"airbyte"` | Airbyte Postgresql username |
| postgresql.tolerations | list | `[]` | Tolerations for postgresql pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| server.affinity | object | `{}` | Affinity and anti-affinity for server pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| server.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| server.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| server.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| server.containerSecurityContext.runAsGroup | int | `1000` |  |
| server.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| server.containerSecurityContext.runAsUser | int | `1000` |  |
| server.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| server.enabled | bool | `true` |  |
| server.env_vars | object | `{}` | Supply extra env variables to main container using simplified notation |
| server.extraContainers | list | `[]` | Additional container for server pods |
| server.extraEnv | list | `[]` | Supply extra env variables to main container using full notation |
| server.extraInitContainers | list | `[]` | Additional init containers for server pods |
| server.extraVolumeMounts | list | `[]` | Additional volumeMounts for server containers |
| server.extraVolumes | list | `[]` | Additional volumes for server pods |
| server.image.pullPolicy | string | `"IfNotPresent"` | the pull policy to use for the airbyte server image |
| server.image.repository | string | `"airbyte/server"` | The repository to use for the airbyte server image. |
| server.livenessProbe.enabled | bool | `true` | Enable livenessProbe on the server |
| server.livenessProbe.failureThreshold | int | `3` | Failure threshold for livenessProbe |
| server.livenessProbe.initialDelaySeconds | int | `30` | Initial delay seconds for livenessProbe |
| server.livenessProbe.periodSeconds | int | `10` | Period seconds for livenessProbe |
| server.livenessProbe.successThreshold | int | `1` | Success threshold for livenessProbe |
| server.livenessProbe.timeoutSeconds | int | `10` | Timeout seconds for livenessProbe |
| server.log.level | string | `"INFO"` | The log level to log at |
| server.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| server.podAnnotations | object | `{}` | Add extra annotations to the server pods |
| server.podLabels | object | `{}` | Add extra labels to the server pods |
| server.podSecurityContext | object | `{"fsGroup":1000}` | Security context for the container |
| server.readinessProbe.enabled | bool | `true` | Enable readinessProbe on the server |
| server.readinessProbe.failureThreshold | int | `3` | Failure threshold for readinessProbe |
| server.readinessProbe.initialDelaySeconds | int | `10` | Initial delay seconds for readinessProbe |
| server.readinessProbe.periodSeconds | int | `10` | Period seconds for readinessProbe |
| server.readinessProbe.successThreshold | int | `1` | Success threshold for readinessProbe |
| server.readinessProbe.timeoutSeconds | int | `10` | Timeout seconds for readinessProbe |
| server.replicaCount | int | `1` | Number of server replicas |
| server.resources.limits | object | `{}` | The resources limits for the server container |
| server.resources.requests | object | `{}` | The requested resources for the server container |
| server.secrets | object | `{}` | Supply additional secrets to container |
| server.tolerations | list | `[]` | Tolerations for server pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| serviceAccount.annotations | object | `{}` | Annotations for service account. Evaluated as a template. Only used if `create` is `true`. |
| serviceAccount.create | bool | `true` | Specifies whether a ServiceAccount should be created |
| serviceAccount.name | string | `"airbyte-admin"` | Name of the service account to use. If not set and create is true, a name is generated using the fullname template. |
| temporal.affinity | object | `{}` | Affinity and anti-affinity for temporal pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| temporal.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| temporal.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| temporal.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| temporal.containerSecurityContext.runAsGroup | int | `1000` |  |
| temporal.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| temporal.containerSecurityContext.runAsUser | int | `1000` |  |
| temporal.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| temporal.enabled | bool | `true` |  |
| temporal.extraContainers | list | `[]` |  |
| temporal.extraEnv | list | `[]` | Additional env vars for temporal pod(s). |
| temporal.extraInitContainers | list | `[]` | Additional InitContainers to initialize the pod |
| temporal.extraVolumeMounts | list | `[]` | Additional volumeMounts for temporal containers |
| temporal.extraVolumes | list | `[]` | Additional volumes for temporal pods |
| temporal.image.pullPolicy | string | `"IfNotPresent"` | The pull policy for the temporal image |
| temporal.image.repository | string | `"temporalio/auto-setup"` | The temporal image repository to use |
| temporal.image.tag | string | `"1.23.0"` | The temporal image tag to use |
| temporal.livenessProbe.enabled | bool | `false` | Enable livenessProbe on the temporal |
| temporal.nodeSelector | object | `{}` | Node labels for temporal pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| temporal.podAnnotations | object | `{}` | Add extra annotations to the temporal pod |
| temporal.podLabels | object | `{}` | Add extra labels to the temporal pod |
| temporal.podSecurityContext | object | `{"fsGroup":1000}` | Security context for the container |
| temporal.readinessProbe.enabled | bool | `false` | Enable readinessProbe on the temporal |
| temporal.replicaCount | int | `1` | The number of temporal replicas to deploy |
| temporal.resources.limits | object | `{}` | The resources limits for temporal pods |
| temporal.resources.requests | object | `{}` | The requested resources for temporal pods |
| temporal.service.port | int | `7233` | The temporal port and exposed kubernetes port |
| temporal.service.type | string | `"ClusterIP"` | The Kubernetes Service Type |
| temporal.tolerations | list | `[]` | Tolerations for temporal pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| version | string | `""` | Sets the AIRBYTE_VERSION environment variable. Defaults to Chart.AppVersion. # If changing the image tags below, you should probably also update this. |
| webapp.affinity | object | `{}` | Affinity and anti-affinity for webapp pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| webapp.connector-builder-server.url | string | `"/connector-builder-api"` |  |
| webapp.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| webapp.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| webapp.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| webapp.containerSecurityContext.runAsGroup | int | `101` |  |
| webapp.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| webapp.containerSecurityContext.runAsUser | int | `101` |  |
| webapp.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| webapp.enabled | bool | `true` |  |
| webapp.env_vars | object | `{}` | Supply extra env variables to main container using simplified notation |
| webapp.extraContainers | list | `[]` | Additional container for server pods |
| webapp.extraEnv | list | `[]` | Supply extra env variables to main container using full notation |
| webapp.extraInitContainers | list | `[]` | Additional init containers for server pods |
| webapp.extraVolumeMounts | list | `[]` | Additional volumeMounts for webapp containers |
| webapp.extraVolumes | list | `[]` | Additional volumes for webapp pods |
| webapp.fullstory.enabled | bool | `false` | Whether or not to enable fullstory |
| webapp.image.pullPolicy | string | `"IfNotPresent"` | The pull policy to use for the airbyte webapp image |
| webapp.image.repository | string | `"airbyte/webapp"` | The repository to use for the airbyte webapp image |
| webapp.ingress.annotations | object | `{}` | Ingress annotations done as key:value pairs |
| webapp.ingress.api | string | `nil` |  |
| webapp.ingress.className | string | `""` | Specifies ingressClassName for clusters >= 1.18+ |
| webapp.ingress.enabled | bool | `false` | Set to true to enable ingress record generation |
| webapp.ingress.hosts | list | `[]` | The list of hostnames to be covered with this ingress record. |
| webapp.ingress.tls | list | `[]` | Custom ingress TLS configuration |
| webapp.ingress.url | string | `"/api/v1/"` | The webapp API url |
| webapp.livenessProbe.enabled | bool | `true` | Enable livenessProbe on the webapp |
| webapp.livenessProbe.failureThreshold | int | `3` | Failure threshold for livenessProbe |
| webapp.livenessProbe.initialDelaySeconds | int | `30` | Initial delay seconds for livenessProbe |
| webapp.livenessProbe.periodSeconds | int | `10` | Period seconds for livenessProbe |
| webapp.livenessProbe.successThreshold | int | `1` | Success threshold for livenessProbe |
| webapp.livenessProbe.timeoutSeconds | int | `1` | Timeout seconds for livenessProbe |
| webapp.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| webapp.podAnnotations | object | `{}` | Add extra annotations to the webapp pods |
| webapp.podLabels | object | `{}` | webapp.podLabels [object] Add extra labels to the webapp pods |
| webapp.podSecurityContext | object | `{"fsGroup":101}` | Security context for the container |
| webapp.readinessProbe.enabled | bool | `true` | Enable readinessProbe on the webapp |
| webapp.readinessProbe.failureThreshold | int | `3` | Failure threshold for readinessProbe |
| webapp.readinessProbe.initialDelaySeconds | int | `10` | Initial delay seconds for readinessProbe |
| webapp.readinessProbe.periodSeconds | int | `10` | Period seconds for readinessProbe |
| webapp.readinessProbe.successThreshold | int | `1` | Success threshold for readinessProbe |
| webapp.readinessProbe.timeoutSeconds | int | `1` | Timeout seconds for readinessProbe |
| webapp.replicaCount | int | `1` | Number of webapp replicas |
| webapp.resources.limits | object | `{}` | The resources limits for the Web container |
| webapp.resources.requests | object | `{}` | The requested resources for the Web container |
| webapp.secrets | object | `{}` | Supply additional secrets to container |
| webapp.service.annotations | object | `{}` | Annotations for the webapp service resource |
| webapp.service.port | int | `80` | The service port to expose the webapp on |
| webapp.service.type | string | `"ClusterIP"` | The service type to use for the webapp service |
| webapp.tolerations | list | `[]` | Tolerations for webapp pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| worker.activityInitialDelayBetweenAttemptsSeconds | string | `""` |  |
| worker.activityMaxAttempt | string | `""` |  |
| worker.activityMaxDelayBetweenAttemptsSeconds | string | `""` |  |
| worker.affinity | object | `{}` | Affinity and anti-affinity for worker pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| worker.containerOrchestrator.image | string | `""` | Orchestrator image |
| worker.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| worker.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| worker.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| worker.containerSecurityContext.runAsGroup | int | `1000` |  |
| worker.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| worker.containerSecurityContext.runAsUser | int | `1000` |  |
| worker.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| worker.debug.enabled | bool | `false` |  |
| worker.enabled | bool | `true` |  |
| worker.extraContainers | list | `[]` | Additional container for worker pods |
| worker.extraEnv | list | `[]` | Additional env vars for worker pods |
| worker.extraVolumeMounts | list | `[]` | Additional volumeMounts for worker containers |
| worker.extraVolumes | list | `[]` | Additional volumes for worker pods |
| worker.hpa.enabled | bool | `false` |  |
| worker.image.pullPolicy | string | `"IfNotPresent"` | the pull policy to use for the airbyte worker image |
| worker.image.repository | string | `"airbyte/worker"` | The repository to use for the airbyte worker image. |
| worker.livenessProbe.enabled | bool | `true` | Enable livenessProbe on the worker |
| worker.livenessProbe.failureThreshold | int | `3` | Failure threshold for livenessProbe |
| worker.livenessProbe.initialDelaySeconds | int | `30` | Initial delay seconds for livenessProbe |
| worker.livenessProbe.periodSeconds | int | `10` | Period seconds for livenessProbe |
| worker.livenessProbe.successThreshold | int | `1` | Success threshold for livenessProbe |
| worker.livenessProbe.timeoutSeconds | int | `1` | Timeout seconds for livenessProbe |
| worker.log.level | string | `"INFO"` |  |
| worker.maxNotifyWorkers | int | `5` |  |
| worker.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| worker.podAnnotations | object | `{}` | Add extra annotations to the worker pods |
| worker.podLabels | object | `{}` | Add extra labels to the worker pods |
| worker.podSecurityContext | object | `{"fsGroup":1000}` | Security context for the container |
| worker.readinessProbe.enabled | bool | `true` | Enable readinessProbe on the worker |
| worker.readinessProbe.failureThreshold | int | `3` | Failure threshold for readinessProbe |
| worker.readinessProbe.initialDelaySeconds | int | `10` | Initial delay seconds for readinessProbe |
| worker.readinessProbe.periodSeconds | int | `10` | Period seconds for readinessProbe |
| worker.readinessProbe.successThreshold | int | `1` | Success threshold for readinessProbe |
| worker.readinessProbe.timeoutSeconds | int | `1` | Timeout seconds for readinessProbe |
| worker.replicaCount | int | `1` | Number of worker replicas |
| worker.resources.limits | object | `{}` |  |
| worker.resources.requests | object | `{}` | The requested resources for the worker container |
| worker.tolerations | list | `[]` | Tolerations for worker pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| workload-api-server.affinity | object | `{}` | Affinity and anti-affinity for webapp pod assignment, see https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#affinity-and-anti-affinity |
| workload-api-server.bearerToken | string | `"token"` |  |
| workload-api-server.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| workload-api-server.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| workload-api-server.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| workload-api-server.containerSecurityContext.runAsGroup | int | `1000` |  |
| workload-api-server.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| workload-api-server.containerSecurityContext.runAsUser | int | `1000` |  |
| workload-api-server.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| workload-api-server.enabled | bool | `false` |  |
| workload-api-server.env_vars | object | `{}` |  |
| workload-api-server.image.pullPolicy | string | `"IfNotPresent"` | The pull policy to use for the airbyte-workload-api-server image |
| workload-api-server.image.repository | string | `"airbyte/workload-api-server"` | The repository to use for the airbyte-workload-api-server image. |
| workload-api-server.ingress.annotations | object | `{}` | Ingress annotations done as key:value pairs |
| workload-api-server.ingress.className | string | `""` | Specifies ingressClassName for clusters >= 1.18+ |
| workload-api-server.ingress.enabled | bool | `false` | Set to true to enable ingress record generation |
| workload-api-server.ingress.hosts | list | `[]` | The list of hostnames to be covered with this ingress record |
| workload-api-server.ingress.tls | list | `[]` | Custom ingress TLS configuration |
| workload-api-server.livenessProbe.enabled | bool | `true` | Enable livenessProbe on the server |
| workload-api-server.livenessProbe.failureThreshold | int | `3` | Failure threshold for livenessProbe |
| workload-api-server.livenessProbe.initialDelaySeconds | int | `30` | Initial delay seconds for livenessProbe |
| workload-api-server.livenessProbe.periodSeconds | int | `10` | Period seconds for livenessProbe |
| workload-api-server.livenessProbe.successThreshold | int | `1` | Success threshold for livenessProbe |
| workload-api-server.livenessProbe.timeoutSeconds | int | `10` | Timeout seconds for livenessProbe |
| workload-api-server.log.level | string | `"INFO"` | The log level at which to log |
| workload-api-server.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| workload-api-server.podSecurityContext | object | `{"fsGroup":1000}` | Security context for the container |
| workload-api-server.readinessProbe.enabled | bool | `true` | Enable readinessProbe on the server |
| workload-api-server.readinessProbe.failureThreshold | int | `3` | Failure threshold for readinessProbe |
| workload-api-server.readinessProbe.initialDelaySeconds | int | `10` | Initial delay seconds for readinessProbe |
| workload-api-server.readinessProbe.periodSeconds | int | `10` | Period seconds for readinessProbe |
| workload-api-server.readinessProbe.successThreshold | int | `1` | Success threshold for readinessProbe |
| workload-api-server.readinessProbe.timeoutSeconds | int | `10` | Timeout seconds for readinessProbe |
| workload-api-server.replicaCount | int | `1` | airbyte-api-server replicas |
| workload-api-server.resources.limits | object | `{}` | The resources limits for the airbyte-workload-api-server container |
| workload-api-server.resources.requests | object | `{}` | The requested resources for the airbyte-workload-api-server container |
| workload-api-server.service.port | int | `8007` |  |
| workload-api-server.tolerations | list | `[]` | Tolerations for webapp pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
| workload-launcher.activityInitialDelayBetweenAttemptsSeconds | string | `""` |  |
| workload-launcher.activityMaxAttempt | string | `""` |  |
| workload-launcher.activityMaxDelayBetweenAttemptsSeconds | string | `""` |  |
| workload-launcher.affinity | object | `{}` |  |
| workload-launcher.containerOrchestrator.enabled | bool | `true` | Enable or disable Orchestrator |
| workload-launcher.containerOrchestrator.image | string | `""` | Orchestrator image |
| workload-launcher.containerSecurityContext.allowPrivilegeEscalation | bool | `false` |  |
| workload-launcher.containerSecurityContext.capabilities.drop[0] | string | `"ALL"` |  |
| workload-launcher.containerSecurityContext.readOnlyRootFilesystem | bool | `false` |  |
| workload-launcher.containerSecurityContext.runAsGroup | int | `1000` |  |
| workload-launcher.containerSecurityContext.runAsNonRoot | bool | `true` |  |
| workload-launcher.containerSecurityContext.runAsUser | int | `1000` |  |
| workload-launcher.containerSecurityContext.seccompProfile.type | string | `"RuntimeDefault"` |  |
| workload-launcher.debug.enabled | bool | `false` |  |
| workload-launcher.enabled | bool | `false` |  |
| workload-launcher.extraContainers | list | `[]` |  |
| workload-launcher.extraEnv | list | `[]` | Additional env vars for workload launcher pods |
| workload-launcher.extraVolumeMounts | list | `[]` | Additional volumeMounts for workload launcher containers |
| workload-launcher.extraVolumes | list | `[]` | Additional volumes for workload launcher pods |
| workload-launcher.hpa.enabled | bool | `false` |  |
| workload-launcher.image.pullPolicy | string | `"IfNotPresent"` | The pull policy to use for the airbyte workload launcher image |
| workload-launcher.image.repository | string | `"airbyte/workload-launcher"` | The repository to use for the airbyte workload launcher image. |
| workload-launcher.livenessProbe.enabled | bool | `true` | Enable livenessProbe on the workload launcher |
| workload-launcher.livenessProbe.failureThreshold | int | `3` | Failure threshold for livenessProbe |
| workload-launcher.livenessProbe.initialDelaySeconds | int | `30` | Initial delay seconds for livenessProbe |
| workload-launcher.livenessProbe.periodSeconds | int | `10` | Period seconds for livenessProbe |
| workload-launcher.livenessProbe.successThreshold | int | `1` | Success threshold for livenessProbe |
| workload-launcher.livenessProbe.timeoutSeconds | int | `1` | Timeout seconds for livenessProbe |
| workload-launcher.log.level | string | `"INFO"` | The log level to log at |
| workload-launcher.maxNotifyWorkers | int | `5` |  |
| workload-launcher.nodeSelector | object | `{}` | Node labels for pod assignment, see https://kubernetes.io/docs/user-guide/node-selection/ |
| workload-launcher.podAnnotations | object | `{}` | Add extra annotations to the workload launcher pods |
| workload-launcher.podLabels | object | `{}` | Add extra labels to the workload launcher pods |
| workload-launcher.podSecurityContext | object | `{"fsGroup":1000}` | Security context for the container |
| workload-launcher.readinessProbe.enabled | bool | `true` | Enable readinessProbe on the workload launcher |
| workload-launcher.readinessProbe.failureThreshold | int | `3` | Failure threshold for readinessProbe |
| workload-launcher.readinessProbe.initialDelaySeconds | int | `10` | Initial delay seconds for readinessProbe |
| workload-launcher.readinessProbe.periodSeconds | int | `10` | Period seconds for readinessProbe |
| workload-launcher.readinessProbe.successThreshold | int | `1` | Success threshold for readinessProbe |
| workload-launcher.readinessProbe.timeoutSeconds | int | `1` | Timeout seconds for readinessProbe |
| workload-launcher.replicaCount | int | `1` | Number of workload launcher replicas |
| workload-launcher.resources.limits | object | `{}` | The resources limits for the workload launcher container |
| workload-launcher.resources.requests | object | `{}` | The requested resources for the workload launcher container |
| workload-launcher.tolerations | list | `[]` | Tolerations for workload launcher pod assignment, see https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |
