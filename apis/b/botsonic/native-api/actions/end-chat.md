# End Chat with Botsonic

Ends a chat conversation in Botsonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/business/bot-data/conversations/:chatId/end-chat`
- **Base URL:** `https://api.botsonic.ai`
- **Official documentation:** [End Chat](https://docs.botsonic.com/reference/end_chat_v1_business_bot_data_conversations__chat_id__end_chat_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | path | `string` | yes | chat_id of the conversation to end. |
| `status` | body | `string` | no | Feedback status for the ended chat. |
| `feedback` | body | `string` | no | Optional feedback for the chat. |
