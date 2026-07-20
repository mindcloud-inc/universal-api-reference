# Get Latest Release with ReleaseNotes

Retrieves the latest release from ReleaseNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/releases/latest`
- **Base URL:** `https://api.releasenotes.io/api/v1`
- **Official documentation:** [Get Latest Release](https://releasenotes.elevio.help/en/articles/87752-retrieving-releases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. |
| `tags` | query | `string` | no | Optional comma-separated tag names to filter the latest matching release, for example article,editor. |
| `released_since` | query | `string` | no | Optional YYYY-MM-DD date to return only the latest release published on or after that date. |
