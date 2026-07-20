# Create Note in First Site with Collected Notes

## Endpoint

- **Method:** `POST`
- **Path:** `/notes/add`
- **Base URL:** `https://collectednotes.com`
- **Official documentation:** [Create Note in First Site](https://collectednotes.com/blog/api#create-a-note-simplified)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `note` | body | `object` | no | — |
| `note.body` | body | `string` | yes | Markdown note content. Start with a markdown heading so Collected Notes can derive the title and path. |
| `note.visibility` | body | `string` | no | — |
