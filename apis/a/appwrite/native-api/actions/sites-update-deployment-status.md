# Update deployment status with Appwrite

Updates the deployment status in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/sites/{siteId}/deployments/{deploymentId}/status`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update deployment status](https://appwrite.io/docs/references/cloud/server-rest/sites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Site ID. |
| `deploymentId` | path | `string` | yes | Deployment ID. |
