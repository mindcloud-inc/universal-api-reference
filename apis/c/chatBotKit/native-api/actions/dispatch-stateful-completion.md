# Dispatch Stateful Completion with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/conversation/{conversationId}/dispatch`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Dispatch Stateful Completion](https://chatbotkit.com/manuals/dispatching-stateful-conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | The ID of the conversation to dispatch |
| `text` | body | `string` | yes | Text to dispatch for completion |
| `entities[]` | body | `array` | no | Entities attached to the dispatched message |
| `functions[]` | body | `array` | no | Functions available during dispatch |
| `extensions` | body | `object` | no | Extensions for the dispatch request |
| `limits` | body | `object` | no | Execution limits for the dispatch request |
| `channelId` | body | `string` | no | Channel ID to dispatch the completion to |
