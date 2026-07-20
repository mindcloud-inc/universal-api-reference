# Open Contact Conversation with Callbell

Reopens a contact conversation in Callbell.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:uuid/conversation/open`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [Open Contact Conversation](https://docs.callbell.eu/api/reference/contacts_api/post_contact_conversation_open/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Unique identifier of the contact whose conversation should be opened. |
