# List Subscribers with ReleaseNotes

Retrieves subscribers from ReleaseNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/subscribers`
- **Base URL:** `https://api.releasenotes.io/api/v1`
- **Official documentation:** [List Subscribers](https://releasenotes.elevio.help/en/articles/87723-listing-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. |
