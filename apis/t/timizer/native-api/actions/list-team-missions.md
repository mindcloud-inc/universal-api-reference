# List Team Missions with Timizer

Retrieves team missions from Timizer.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/admin-teams/:teamId/missions`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [List Team Missions](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `month` | query | `string` | no | Year also needs to be set if Month is used. |
| `teamId` | path | `string` | no | ID of the team. |
| `year` | query | `string` | no | Month also needs to be set if Year is used. |
