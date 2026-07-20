# Create Message with Twist

Creates a new message in a Twist conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversation_messages/add`
- **Base URL:** `https://api.twist.com/api/v3`
- **Official documentation:** [Create Message](https://developer.twist.com/v3/#add-message-to-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachments` | query | `string` | no | JSON-encoded list of attachment objects returned by Upload attachment. |
| `content` | query | `string` | yes | The content of the new message. |
| `conversation_id` | query | `number` | yes | The id of the conversation. |
