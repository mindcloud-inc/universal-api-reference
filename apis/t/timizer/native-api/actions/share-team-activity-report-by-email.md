# Share Team Activity Report by Email with Timizer

Shares a team activity report by email in Timizer.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/admin-teams/:teamId/activity-reports/:activityReportId/share-by-email`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [Share Team Activity Report by Email](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityReportId` | path | `number` | yes | ID of the activity report. |
| `contactId` | body | `number` | no | Optional contact ID. Defaults to the activity report client contact. |
| `teamId` | path | `number` | yes | ID of the team. |
