# Get Team Activity Report with Timizer

Retrieves a team activity report from Timizer.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/admin-teams/:teamId/activity-reports/:activityReportId`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [Get Team Activity Report](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityReportId` | path | `string` | no | ID of the activity report. |
| `teamId` | path | `string` | no | ID of the team. |
