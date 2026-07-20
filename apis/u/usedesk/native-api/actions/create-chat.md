# Create Chat with Usedesk

Creates a new chat in Usedesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/addMessage`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Create Chat](https://api.usedocs.com/article/51394)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | body | `string` | no | Existing chat ID. Omit to create a new chat. |
| `company_id` | body | `number` | yes | Your company ID. |
| `message.from.client_id` | body | `string` | no | Client ID bound to the chat. |
| `message.from.email` | body | `string` | no | Client email. |
| `message.from.name` | body | `string` | no | Client name. |
| `channel_id` | body | `number` | yes | Chat channel ID. |
| `message.text` | body | `string` | yes | Message text. |
