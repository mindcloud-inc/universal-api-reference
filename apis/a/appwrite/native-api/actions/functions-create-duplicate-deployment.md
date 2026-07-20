# Create duplicate deployment with Appwrite

Creates a new duplicate deployment in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/functions/{functionId}/deployments/duplicate`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create duplicate deployment](https://appwrite.io/docs/references/cloud/server-rest/functions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Function ID. |
| `deploymentId` | body | `string` | yes | Deployment ID. |
| `buildId` | body | `string` | no | Build unique ID. |
