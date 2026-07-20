# Get Release with ReleaseNotes

Retrieves a release from ReleaseNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/releases/:releaseId`
- **Base URL:** `https://api.releasenotes.io/api/v1`
- **Official documentation:** [Get Release](https://releasenotes.elevio.help/en/articles/87752-retrieving-releases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. |
| `releaseId` | path | `string` | yes | The release ID returned as id from the ReleaseNotes releases endpoints or shown in the hosted release URL. |
