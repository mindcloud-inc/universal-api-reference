# Get deployment download with Appwrite

Retrieves the deployment download from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/{siteId}/deployments/{deploymentId}/download`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get deployment download](https://appwrite.io/docs/references/cloud/server-rest/sites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Site ID. |
| `deploymentId` | path | `string` | yes | Deployment ID. |
| `type` | query | `string` | no | Deployment file to download. Can be: "source", "output". |
