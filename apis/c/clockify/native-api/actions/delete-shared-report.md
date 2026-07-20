# Delete Shared Report with Clockify

Deletes an existing shared report from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/shared-reports/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Shared Report](https://docs.developer.clockify.me/#tag/Shared-Report/operation/deleteSharedReportV1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `workspaceId` | path | `list<string>` | yes |
