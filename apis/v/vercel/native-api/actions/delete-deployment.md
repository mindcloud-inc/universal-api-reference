# Delete Deployment with Vercel

Deletes an existing deployment from Vercel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v13/deployments/:id`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Delete Deployment](https://docs.vercel.com/docs/rest-api/reference/endpoints/deployments/delete-a-deployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the deployment. |
