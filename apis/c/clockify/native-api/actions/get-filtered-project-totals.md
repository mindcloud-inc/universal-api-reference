# Get Filtered Project Totals with Clockify

Retrieves filtered project totals from Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/scheduling/assignments/projects/totals`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Filtered Project Totals](https://docs.developer.clockify.me/#tag/Scheduling/operation/getFilteredProjectTotals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | body | `date` | yes | — |
| `page` | body | `number` | no | — |
| `pageSize` | body | `number` | no | — |
| `search` | body | `string` | no | — |
| `start` | body | `date` | yes | — |
| `statusFilter` | body | `list` | no | Accepted values: `ALL`, `PUBLISHED`, `UNPUBLISHED`. |
| `workspaceId` | path | `list<string>` | yes | — |
