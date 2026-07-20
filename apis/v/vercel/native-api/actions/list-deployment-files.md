# List Deployment Files with Vercel

Retrieves all deployment files from Vercel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v6/deployments/:id/files`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [List Deployment Files](https://docs.vercel.com/docs/rest-api/reference/endpoints/deployments/list-deployment-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the deployment. |
