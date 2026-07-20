# Create Note with Collected Notes

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/:siteId/notes`
- **Base URL:** `https://collectednotes.com`
- **Official documentation:** [Create Note](https://collectednotes.com/blog/api#create-a-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `number` | yes | The Collected Notes site ID. |
| `note` | body | `object` | no | — |
| `note.body` | body | `string` | yes | Markdown note content. Start with a markdown heading so Collected Notes can derive the title and path. |
| `note.visibility` | body | `string` | no | — |
