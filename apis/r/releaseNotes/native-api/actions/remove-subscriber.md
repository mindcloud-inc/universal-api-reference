# Remove Subscriber with ReleaseNotes

Deletes a subscriber from ReleaseNotes.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/subscribers/remove`
- **Base URL:** `https://api.releasenotes.io/api/v1`
- **Official documentation:** [Remove Subscriber](https://releasenotes.elevio.help/en/articles/87725-deleting-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. |
| `value` | body | `string` | yes | The subscriber email address or value to remove. |
