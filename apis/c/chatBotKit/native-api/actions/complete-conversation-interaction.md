# Complete Conversation Interaction with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/conversation/complete`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Complete Conversation Interaction](https://chatbotkit.com/manuals/conversation-flow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array` | yes | Messages to complete |
| `attachments[]` | body | `array` | no | Attachments for the completion request |
| `contactId` | body | `object` | no | Contact payload for the completion request |
| `functions[]` | body | `array` | no | Functions available during completion |
| `extensions` | body | `object` | no | Extensions for the completion request |
| `limits` | body | `object` | no | Execution limits for the completion request |
