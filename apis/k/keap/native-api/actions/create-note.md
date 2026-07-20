# Create Note with Keap

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/{contact_id}/notes`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [Create Note](https://developer.keap.com/docs/restv2/#tag/Note/operation/createNote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The unique identifier of the contact. |
| `is_pinned` | body | `string` | no | — |
| `text` | body | `string` | no | — |
| `title` | body | `string` | no | — |
| `type` | body | `string` | no | — |
| `user_id` | body | `string` | yes | — |
