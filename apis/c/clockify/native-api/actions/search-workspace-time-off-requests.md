# Search Workspace Time Off Requests with Clockify

Finds workspace time off requests in Clockify by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/time-off/requests`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Search Workspace Time Off Requests](https://docs.developer.clockify.me/#tag/Time-Off/operation/getTimeOffRequest)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `end` | body | `date` | no |
| `page` | body | `number` | no |
| `pageSize` | body | `number` | no |
| `start` | body | `date` | no |
| `statuses[]` | body | `array<string>` | no |
| `userGroups[]` | body | `array<string>` | no |
| `users[]` | body | `array<string>` | no |
