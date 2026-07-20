# Create Deployment with Vercel

Creates a new deployment in Vercel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v13/deployments`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Create Deployment](https://docs.vercel.com/docs/rest-api/reference/endpoints/deployments/create-a-new-deployment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deploymentId` | body | `string` | yes | An existing deployment id to redeploy. |
| `name` | body | `string` | yes | The project name used in the deployment URL. |
| `withLatestCommit` | body | `boolean` | no | Force the latest commit when redeploying an existing deployment. |
