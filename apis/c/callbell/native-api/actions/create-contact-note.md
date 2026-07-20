# Create Contact Note with Callbell

Creates a conversation note for a Callbell contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:uuid/conversation/note`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [Create Contact Note](https://docs.callbell.eu/api/reference/contacts_api/post_contact_conversation_create_note/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to save as a conversation note. |
| `uuid` | path | `string` | yes | Unique identifier of the contact whose conversation note should be created. |
