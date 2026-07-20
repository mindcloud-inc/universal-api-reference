# List Team Activity Reports with Timizer

Retrieves team activity reports from Timizer.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/admin-teams/:teamId/activity-reports`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [List Team Activity Reports](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | query | `string` | no | ID of the client. |
| `missionId` | query | `string` | no | ID of the mission. |
| `month` | query | `string` | no | The target month. Year must also be present. |
| `since` | query | `string` | no | A unix timestamp. Only the ActivityReports with year and month greater than or equal to the given timestamp will be returned. |
| `teamId` | path | `string` | no | ID of the team. |
| `workflowStepName` | query | `string` | no | Filter by workflow step name. Can be set multiple times. |
| `year` | query | `string` | no | The target year. Month must also be present. |
