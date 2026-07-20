# Update Conversation with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/conversation/{conversationId}/update`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Update Conversation](https://chatbotkit.com/manuals/conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | The ID of the conversation to update |
| `name` | body | `string` | no | Name of the conversation |
| `description` | body | `string` | no | Description of the conversation |
| `meta` | body | `object` | no | Metadata for the conversation |
| `contactId` | body | `string` | no | Contact ID for the conversation |
| `taskId` | body | `string` | no | Task ID for the conversation |
| `spaceId` | body | `string` | no | Space ID for the conversation |
