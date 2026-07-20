# Send Conversation Message with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/conversation/{conversationId}/send`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Send Conversation Message](https://chatbotkit.com/manuals/conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | The ID of the conversation to send the message to |
| `text` | body | `string` | yes | Text of the message to send |
| `entities[]` | body | `array` | no | Entities attached to the message |
| `functions[]` | body | `array` | no | Functions available during send |
| `extensions` | body | `object` | no | Extensions for the send request |
