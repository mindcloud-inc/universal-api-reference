# Close Contact Conversation with Callbell

Closes a contact conversation in Callbell.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:uuid/conversation/close`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [Close Contact Conversation](https://docs.callbell.eu/api/reference/contacts_api/post_contact_conversation_close/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Unique identifier of the contact whose conversation should be closed. |
