# Update Note with Collected Notes

## Endpoint

- **Method:** `PUT`
- **Path:** `/sites/:siteId/notes/:noteId`
- **Base URL:** `https://collectednotes.com`
- **Official documentation:** [Update Note](https://collectednotes.com/blog/api#update-a-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `number` | yes | The Collected Notes site ID. |
| `noteId` | path | `number` | yes | The Collected Notes note ID. |
| `note` | body | `object` | no | — |
| `note.body` | body | `string` | no | Markdown note content. Start with a markdown heading so Collected Notes can derive the title and path. |
| `note.visibility` | body | `string` | no | — |
