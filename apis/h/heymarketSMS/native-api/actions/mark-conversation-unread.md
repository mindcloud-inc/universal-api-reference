# Mark Conversation Unread with Heymarket SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/conversations/unread`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Mark Conversation Unread](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | body | `number` | yes | Unique identifier of the inbox. |
| `user_id` | body | `number` | yes | Unique identifier of the user. |
| `target` | body | `string` | no | Phone number for the conversation. |
| `targets[]` | body | `array<string>` | no | Phone numbers for a group MMS conversation. |
