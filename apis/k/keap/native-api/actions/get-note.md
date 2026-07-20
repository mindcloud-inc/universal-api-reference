# Get Note with Keap

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:contact_id/notes/:note_id`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [Get Note](https://developer.keap.com/docs/restv2/#tag/Note/operation/getNote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The unique identifier of the contact. |
| `note_id` | path | `string` | yes | The unique identifier of the note. |
