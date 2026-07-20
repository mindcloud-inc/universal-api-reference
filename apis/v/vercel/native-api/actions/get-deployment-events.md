# Get Deployment Events with Vercel

Retrieves deployment events for a Vercel deployment.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/deployments/:idOrUrl/events`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Get Deployment Events](https://docs.vercel.com/docs/rest-api/reference/endpoints/deployments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrUrl` | path | `string` | yes | The unique identifier or hostname of the deployment. |
