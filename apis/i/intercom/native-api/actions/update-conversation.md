# Update Conversation with Intercom

## Endpoint

- **Method:** `PUT`
- **Path:** `/conversations/:conversation_id`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Update Conversation](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/updateconversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Intercom conversation identifier |
| `read` | body | `boolean` | no | Mark the conversation as read in Intercom |
| `title` | body | `string` | no | The title of the conversation |
| `custom_attributes` | body | `object` | no | Custom attributes to update on the conversation |
