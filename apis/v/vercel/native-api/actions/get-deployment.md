# Get Deployment with Vercel

Retrieves a deployment record from Vercel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v13/deployments/:idOrUrl`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Get Deployment](https://docs.vercel.com/docs/rest-api/reference/endpoints/deployments/get-a-deployment-by-id-or-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrUrl` | path | `string` | yes | The unique identifier or hostname of the deployment. |
| `withGitRepoInfo` | query | `string` | no | Whether to add in gitRepo information. |
