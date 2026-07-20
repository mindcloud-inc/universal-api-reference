# Create Conversation with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/conversation/create`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Create Conversation](https://chatbotkit.com/manuals/conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name of the conversation |
| `description` | body | `string` | no | Description of the conversation |
| `meta` | body | `object` | no | Metadata for the conversation |
| `contactId` | body | `string` | no | Contact ID for the conversation |
| `taskId` | body | `string` | no | Task ID for the conversation |
| `spaceId` | body | `string` | no | Space ID for the conversation |
| `messages[]` | body | `array` | no | Messages used to create the conversation |
