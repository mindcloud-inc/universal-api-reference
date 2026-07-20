# Delete Holiday with Clockify

Deletes an existing holiday from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/holidays/:holidayId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Holiday](https://docs.developer.clockify.me/#tag/Holiday/operation/deleteHoliday)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `holidayId` | path | `string<string>` | yes |
