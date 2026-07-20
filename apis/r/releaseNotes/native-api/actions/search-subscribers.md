# Search Subscribers with ReleaseNotes

Finds subscribers in ReleaseNotes by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/subscribers/search`
- **Base URL:** `https://api.releasenotes.io/api/v1`
- **Official documentation:** [Search Subscribers](https://releasenotes.elevio.help/en/articles/87724-searching-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. |
| `q` | body | `string` | yes | The email address or partial subscriber value to search for. |
