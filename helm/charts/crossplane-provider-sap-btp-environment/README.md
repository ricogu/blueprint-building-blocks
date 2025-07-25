

# crossplane-provider-sap-btp-environment

![Version: 0.0.18](https://img.shields.io/badge/Version-0.0.18-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.0.1](https://img.shields.io/badge/AppVersion-0.0.1-informational?style=flat-square)

A Helm Chart to template crossplane manifests to manage Cloud Foundry or BTP Kyma environments on BTP.

**Homepage:** <https://github.com/openmcp-project/blueprints>

## Source Code

* <https://github.com/openmcp-project/blueprint-building-blocks>
* <https://pages.github.tools.sap/cloud-orchestration/browser/Providers/provider-btp/environment.btp.sap.crossplane.io/cloudfoundryenvironment/v1alpha1>
* <https://pages.github.tools.sap/cloud-orchestration/browser/Providers/provider-btp/environment.btp.sap.crossplane.io/kymaenvironment/v1alpha1>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| cloudFoundryEnvironments | list | object | cloudFoundryEnvironments contains configuration of [cloudfoundry Environments](https://pages.github.tools.sap/cloud-orchestration/browser/Providers/provider-btp-account/environment.btp.sap.crossplane.io/cloudfoundryenvironment/v1alpha1). |
| cloudFoundryEnvironments[0] | object | `{"btpSapCrossplaneProviderConfigRefName":"","cloudManagementRef":{"name":"dev-eu01"},"forProvider":{"initialOrgManagers":[""],"landscape":""},"name":"","subaccountRef":{"name":"dev-eu01"},"writeConnectionSecretToRef":[]}` | btpSapCrossplaneProviderConfigRefName defines crossplane provider configuration reference name (identifier) of a ...! |
| cloudFoundryEnvironments[0].writeConnectionSecretToRef | list | `[]` | *optional* - When a Crossplane Provider creates a managed resource it may generate resource-specific details, like usernames, passwords or connection details like an IP address.   Crossplane stores these details in a Kubernetes Secret object specified by the `writeConnectionSecretToRef` values. Learn more about Crossplane concept [Managed Resources Fields](https://docs.crossplane.io/latest/concepts/managed-resources/#writeconnectionsecrettoref)! |
| kymaEnvironmentBindings[0].btpSapCrossplaneProviderConfigRefName | string | `""` |  |
| kymaEnvironmentBindings[0].cloudManagementRef.name | string | `"dev-eu01"` |  |
| kymaEnvironmentBindings[0].forProvider.rotationInterval | string | `"6h"` |  |
| kymaEnvironmentBindings[0].forProvider.ttl | string | `"8h"` |  |
| kymaEnvironmentBindings[0].kymaEnvironmentRef.name | string | `"my-kyma-instance"` |  |
| kymaEnvironmentBindings[0].name | string | `""` |  |
| kymaEnvironmentBindings[0].writeConnectionSecretToRef | object | `{"name":"demo-kyma-binding-local","namespace":"default"}` | *optional* - When a Crossplane Provider creates a managed resource it may generate resource-specific details, like usernames, passwords or connection details like an IP address.   Crossplane stores these details in a Kubernetes Secret object specified by the `writeConnectionSecretToRef` values. Learn more about Crossplane concept [Managed Resources Fields](https://docs.crossplane.io/latest/concepts/managed-resources/#writeconnectionsecrettoref)! |
| kymaEnvironments[0].btpSapCrossplaneProviderConfigRefName | string | `""` |  |
| kymaEnvironments[0].cloudManagementRef.name | string | `"dev-eu01"` |  |
| kymaEnvironments[0].forProvider.administrators[0] | string | `"...@sap.com"` |  |
| kymaEnvironments[0].forProvider.autoScalerMax | int | `3` |  |
| kymaEnvironments[0].forProvider.autoScalerMin | int | `3` |  |
| kymaEnvironments[0].forProvider.machineType | string | `"m5.xlarge"` |  |
| kymaEnvironments[0].forProvider.oidc.clientID | string | `"<your client id>"` |  |
| kymaEnvironments[0].forProvider.oidc.groupsClaim | string | `"groups"` |  |
| kymaEnvironments[0].forProvider.oidc.issuerURL | string | `"https://<IAS host>.accounts400.ondemand.com"` |  |
| kymaEnvironments[0].forProvider.oidc.signingAlgs[0] | string | `"RS256"` |  |
| kymaEnvironments[0].forProvider.oidc.usernameClaim | string | `"email"` |  |
| kymaEnvironments[0].forProvider.oidc.usernamePrefix | string | `"-"` |  |
| kymaEnvironments[0].forProvider.parameters | string | `nil` |  |
| kymaEnvironments[0].forProvider.region | string | `"eu-west-2"` |  |
| kymaEnvironments[0].name | string | `""` |  |
| kymaEnvironments[0].planName | string | `"aws"` |  |
| kymaEnvironments[0].subaccountRef.name | string | `"dev-eu01"` |  |
| kymaEnvironments[0].writeConnectionSecretToRef | object | `{"name":"demo-kyma-kubeconfig-local","namespace":"default"}` | *optional* - When a Crossplane Provider creates a managed resource it may generate resource-specific details, like usernames, passwords or connection details like an IP address.   Crossplane stores these details in a Kubernetes Secret object specified by the `writeConnectionSecretToRef` values. Learn more about Crossplane concept [Managed Resources Fields](https://docs.crossplane.io/latest/concepts/managed-resources/#writeconnectionsecrettoref)! |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)