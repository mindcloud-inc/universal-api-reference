# List Deployment Errors with PixieBrix

Retrieves recent deployment errors from PixieBrix.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/deployments/:deployment_pk/errors/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [List Deployment Errors](https://app.pixiebrix.com/api/docs/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deployment_pk` | path | `string` | yes | PixieBrix deployment identifier. |
