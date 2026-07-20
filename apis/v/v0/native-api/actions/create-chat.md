# Create Chat with v0

Creates a new chat in v0.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chats`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Create Chat](https://v0.app/docs/api/platform/reference/chats/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | The prompt to send when creating a new chat. |
| `projectId` | body | `string` | no | Associates the chat with a specific project in your workspace. |
| `system` | body | `string` | no | — |
| `attachments[]` | body | `array<object>` | no | — |
| `chatPrivacy` | body | `string` | no | — |
| `modelConfiguration` | body | `object` | no | — |
| `responseMode` | body | `string` | no | — |
| `thinking` | body | `boolean` | no | — |
| `imageGenerations` | body | `boolean` | no | — |
| `designSystemId` | body | `string` | no | — |
| `modelId` | body | `string` | no | — |
