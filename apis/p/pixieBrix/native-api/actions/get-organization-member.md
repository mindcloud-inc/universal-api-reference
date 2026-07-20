# Get Organization Member with PixieBrix

Retrieves an organization member from PixieBrix.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/organizations/:organization_pk/members/:id/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [Get Organization Member](https://app.pixiebrix.com/api/docs/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | PixieBrix user UUID for the organization member. |
| `organization_pk` | path | `string` | yes | PixieBrix organization identifier. |
