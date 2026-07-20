# Update function's deployment with Appwrite

Updates a function deployment in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/functions/{functionId}/deployment`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update function's deployment](https://appwrite.io/docs/references/cloud/server-rest/functions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Function ID. |
| `deploymentId` | body | `string` | yes | Deployment ID. |
