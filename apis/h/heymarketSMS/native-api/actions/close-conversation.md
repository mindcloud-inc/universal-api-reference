# Close Conversation with Heymarket SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/conversations/close`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Close Conversation](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | body | `number` | yes | Unique identifier of the inbox. |
| `user_id` | body | `number` | yes | Unique identifier of the user closing the conversation. |
| `target` | body | `string` | no | Phone number corresponding to the conversation in E.164 format without the plus sign. |
| `chat_id` | body | `number` | no | Unique identifier of the conversation. |
