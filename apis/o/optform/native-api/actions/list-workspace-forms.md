# List Workspace Forms with Optform

Retrieves forms from a specific Optform workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Form/all/:workspaceId`
- **Base URL:** `https://optform.azure-api.net`
- **Official documentation:** [List Workspace Forms](https://optform.com/help/api/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes |
