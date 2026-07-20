# List Webhooks with ReleaseNotes

Retrieves webhooks from ReleaseNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/webhooks`
- **Base URL:** `https://api.releasenotes.io/api/v1`
- **Official documentation:** [List Webhooks](https://releasenotes.elevio.help/en/articles/87801-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. |
