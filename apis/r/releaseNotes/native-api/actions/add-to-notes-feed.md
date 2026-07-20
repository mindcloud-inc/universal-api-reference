# Add to Notes Feed with ReleaseNotes

Creates a new notes feed item in ReleaseNotes.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/notesbucket/append`
- **Base URL:** `https://api.releasenotes.io/api/v1`
- **Official documentation:** [Add to Notes Feed](https://releasenotes.elevio.help/en/articles/87754-adding-to-your-notes-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. |
| `notes` | body | `string` | yes | The note content to append to the project's notes feed. |
| `title` | body | `string` | no | Optional title for the notes feed item. |
| `external_id` | body | `string` | no | Optional external identifier for idempotent note appends. |
| `external_link` | body | `string` | no | Optional URL to associate with the notes feed item. |
| `attribution` | body | `string` | no | Optional attribution text shown with the notes feed item. |
