# List Package Versions with PixieBrix

Retrieves versions for a PixieBrix package.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/bricks/:id/versions/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [List Package Versions](https://docs.pixiebrix.com/developer-api/package-management-apis)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | PixieBrix package UUID. |
