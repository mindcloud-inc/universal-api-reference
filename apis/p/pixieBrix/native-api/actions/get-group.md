# Get Group with PixieBrix

Retrieves a group from PixieBrix.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/groups/:id/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [Get Group](https://app.pixiebrix.com/api/docs/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | PixieBrix group identifier. |
