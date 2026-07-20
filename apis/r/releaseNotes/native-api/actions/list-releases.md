# List Releases with ReleaseNotes

Retrieves releases from ReleaseNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/releases`
- **Base URL:** `https://api.releasenotes.io/api/v1`
- **Official documentation:** [List Releases](https://releasenotes.elevio.help/en/articles/87752-retrieving-releases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. |
| `page` | query | `string` | no | Optional page number for paginated release results. |
| `tags` | query | `string` | no | Optional comma-separated tag names to filter releases, for example article,editor. |
| `released_since` | query | `string` | no | Optional YYYY-MM-DD date to return only releases published on or after that date. |
