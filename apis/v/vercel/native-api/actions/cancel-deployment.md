# Cancel Deployment with Vercel

Cancels an existing deployment in Vercel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v12/deployments/:id/cancel`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Cancel Deployment](https://docs.vercel.com/docs/rest-api/reference/endpoints/deployments/cancel-a-deployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the deployment. |
