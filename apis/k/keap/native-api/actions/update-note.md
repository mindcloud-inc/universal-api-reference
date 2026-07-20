# Update Note with Keap

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/{contact_id}/notes/{note_id}`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [Update Note](https://developer.keap.com/docs/restv2/#tag/Note/operation/updateNote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The unique identifier of the contact. |
| `is_pinned` | body | `string` | no | — |
| `note_id` | path | `string` | yes | The unique identifier of the note. |
| `text` | body | `string` | no | — |
| `title` | body | `string` | no | — |
| `type` | body | `string` | no | — |
| `update_mask` | query | `string` | no | — |
| `user_id` | body | `string` | yes | — |
