# Update deployment status with Appwrite

Updates the deployment status in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/functions/{functionId}/deployments/{deploymentId}/status`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update deployment status](https://appwrite.io/docs/references/cloud/server-rest/functions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Function ID. |
| `deploymentId` | path | `string` | yes | Deployment ID. |
