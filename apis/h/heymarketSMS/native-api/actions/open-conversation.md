# Open Conversation with Heymarket SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/conversations/open`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Open Conversation](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | body | `number` | yes | Unique identifier of the inbox. |
| `user_id` | body | `number` | yes | Unique identifier of the user opening the conversation. |
| `chat_id` | body | `number` | no | Unique identifier of the conversation. |
| `target` | body | `string` | no | Phone number for the conversation. |
| `targets[]` | body | `array<string>` | no | Phone numbers for a group MMS conversation. |
