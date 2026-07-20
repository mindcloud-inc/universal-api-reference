# Get deployment download with Appwrite

Retrieves the deployment download from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/functions/{functionId}/deployments/{deploymentId}/download`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get deployment download](https://appwrite.io/docs/references/cloud/server-rest/functions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Function ID. |
| `deploymentId` | path | `string` | yes | Deployment ID. |
| `type` | query | `string` | no | Deployment file to download. Can be: "source", "output". |
