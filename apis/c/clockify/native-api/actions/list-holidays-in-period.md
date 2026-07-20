# List Holidays in Period with Clockify

Lists holidays in a period in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/holidays/in-period`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Holidays in Period](https://docs.developer.clockify.me/#tag/Holiday/operation/getHolidaysInPeriod)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `assigned-to` | query | `string` | yes |
| `end` | query | `string` | yes |
| `start` | query | `string` | yes |
