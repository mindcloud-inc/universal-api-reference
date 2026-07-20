# Manage Conversation Part with Intercom

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:conversation_id/parts`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Manage Conversation Part](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/manageconversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Intercom conversation identifier |
| `message_type` | body | `string` | yes | Conversation action type (comment/open/close/snoozed) |
| `admin_id` | body | `string` | yes | Admin performing the conversation action |
| `body` | body | `string` | no | Optional message for the action |
