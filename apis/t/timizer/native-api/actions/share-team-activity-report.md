# Share Team Activity Report with Timizer

Creates a share link for a team activity report in Timizer.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/admin-teams/:teamId/activity-reports/:activityReportId/share`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [Share Team Activity Report](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityReportId` | path | `string` | no | ID of the activity report. |
| `teamId` | path | `string` | no | ID of the team. |
