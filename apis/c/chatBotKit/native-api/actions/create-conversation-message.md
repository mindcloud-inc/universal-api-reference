# Create Conversation Message with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/conversation/{conversationId}/message/create`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Create Conversation Message](https://chatbotkit.com/manuals/conversation-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | The ID of the conversation |
| `name` | body | `string` | no | Name of the message |
| `description` | body | `string` | no | Description of the message |
| `meta` | body | `object` | no | Metadata for the message |
| `type` | body | `list` | yes | Type of the message Accepted values: `activity`, `backstory`, `bot`, `context`, `instruction`, `reasoning`, `user`. |
| `text` | body | `string` | yes | Text of the message |
| `entities[]` | body | `array` | no | Entities attached to the message |
