# Send Message with v0

Sends a message to an existing v0 chat.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chats/:chatId/messages`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Send Message](https://v0.app/docs/api/platform/reference/chats/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The ID of the chat that should receive the message. |
| `message` | body | `string` | yes | The prompt or instruction to send to the chat. |
| `system` | body | `string` | no | — |
| `attachments[]` | body | `array<object>` | no | — |
| `modelConfiguration` | body | `object` | no | — |
| `responseMode` | body | `string` | no | — |
| `thinking` | body | `boolean` | no | — |
| `imageGenerations` | body | `boolean` | no | — |
| `mcpServerIds[]` | body | `array<string>` | no | — |
| `modelId` | body | `string` | no | — |
