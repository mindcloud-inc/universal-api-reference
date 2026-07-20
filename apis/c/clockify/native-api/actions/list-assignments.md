# List Assignments with Clockify

Lists all scheduling assignments in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/scheduling/assignments/all`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Assignments](https://docs.developer.clockify.me/#tag/Scheduling/operation/getAllAssignments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | yes | — |
| `name` | query | `string` | no | — |
| `page` | query | `number` | no | — |
| `page-size` | query | `number` | no | — |
| `sort-column` | query | `list` | no | Accepted values: `ID`, `PROJECT`, `USER`. |
| `sort-order` | query | `list` | no | Accepted values: `ASCENDING`, `DESCENDING`. |
| `start` | query | `string` | yes | — |
| `workspaceId` | path | `list<string>` | yes | — |
