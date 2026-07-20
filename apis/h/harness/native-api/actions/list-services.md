# List Services with Harness

Retrieves services from Harness.

## Endpoint

- **Method:** `GET`
- **Path:** `/ng/api/servicesV2`
- **Base URL:** `https://app.harness.io/gateway`
- **Official documentation:** [List Services](https://apidocs.harness.io/services/getservicelist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deploymentTemplateIdentifier` | query | `string` | no | Deployment template identifier filter. |
| `gitOpsEnabled` | query | `boolean` | no | Filter by GitOps enabled services. |
| `includeAllServicesAccessibleAtScope` | query | `boolean` | no | Include all accessible services at the current scope. |
| `searchTerm` | query | `string` | no | Search term to include in the list response. |
| `serviceIdentifiers` | query | `list<string>` | no | Service identifiers to include. |
| `sort` | query | `string` | no | Sorting criteria for the services list. |
| `type` | query | `string` | no | Service type filter. |
| `versionLabel` | query | `string` | no | Version label filter. |
