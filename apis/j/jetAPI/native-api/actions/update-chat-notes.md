# Update Chat Notes with JetAPI

Updates existing chat notes in JetAPI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/developer_chat/conversations/notes`
- **Base URL:** `https://api.jetapi.io`
- **Official documentation:** [Update Chat Notes](https://docs.jetapi.io/#fde64a3c-12e8-4953-b4ef-363078153aaa)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | yes | Phone number to identify the conversation. |
| `notes[].title` | body | `string` | yes | Chat note title. |
| `notes[].body` | body | `string` | yes | Chat note content. |
| `tdlib_username` | body | `string` | no | Optional Telegram username identifier. |
| `tdlib_user_id` | body | `number` | no | Optional Telegram user ID identifier. |
