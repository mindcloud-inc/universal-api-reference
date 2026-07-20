# Reply Conversation with Intercom

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:conversation_id/reply`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Reply Conversation](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/replyconversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Intercom conversation identifier |
| `admin_id` | body | `string` | yes | Admin sending the reply |
| `body` | body | `string` | yes | Reply content |
