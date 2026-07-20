# Get Deployment with PixieBrix

Retrieves a deployment from PixieBrix.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/deployments/:id/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [Get Deployment](https://docs.pixiebrix.com/developer-api/deployment-apis)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | PixieBrix deployment identifier. |
