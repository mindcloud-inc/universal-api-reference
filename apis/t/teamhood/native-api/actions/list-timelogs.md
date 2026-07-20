# List Timelogs with Teamhood

Retrieves timelogs from Teamhood by request filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/timelogs`
- **Base URL:** `https://api-mindcloud1.teamhood.com/api/v1`
- **Official documentation:** [List Timelogs](https://api-mindcloud1.teamhood.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | body | `string` | no | The inclusive timelog window end in ISO 8601 format. |
| `startDate` | body | `string` | no | The inclusive timelog window start in ISO 8601 format. |
| `workspaceId` | body | `string` | no | The workspace to query timelogs for. |
