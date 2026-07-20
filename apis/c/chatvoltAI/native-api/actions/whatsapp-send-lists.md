# Send List with Chatvolt AI

Sends an interactive list through Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/interactive/send-lists`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Send List](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/send-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | The ID of the agent. |
| `conversationId` | body | `string` | yes | The ID of the conversation. |
| `header_text` | body | `string` | no | Optional header text. |
| `body_text` | body | `string` | yes | Main message body. |
| `footer_text` | body | `string` | no | Optional footer text. |
| `button_text` | body | `string` | yes | Text for the button that opens the list. |
| `list_title` | body | `string` | no | Title for the list (mainly for Z-API). |
