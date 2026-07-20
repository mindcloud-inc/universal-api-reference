# Get Package with PixieBrix

Retrieves a package from PixieBrix.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/bricks/:id/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [Get Package](https://docs.pixiebrix.com/developer-api/package-management-apis)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | PixieBrix package UUID. |
