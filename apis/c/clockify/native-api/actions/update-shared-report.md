# Update Shared Report with Clockify

Updates an existing shared report in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/shared-reports/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Shared Report](https://docs.developer.clockify.me/#tag/Shared-Report/operation/updateSharedReportV1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fixedDate` | body | `boolean` | no |
| `id` | path | `string` | yes |
| `isPublic` | body | `boolean` | no |
| `name` | body | `string` | yes |
| `visibleToUserGroups[]` | body | `array<string>` | no |
| `visibleToUsers[]` | body | `array<string>` | no |
| `workspaceId` | path | `list<string>` | yes |
