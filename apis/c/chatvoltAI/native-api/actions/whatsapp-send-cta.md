# Send CTA with Chatvolt AI

Sends an interactive CTA through Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/interactive/send-cta`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Send CTA](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/send-cta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | The ID of the agent. |
| `conversationId` | body | `string` | yes | The ID of the conversation. |
| `header_text` | body | `string` | no | Optional header text. |
| `body_text` | body | `string` | yes | Main message body. |
| `footer_text` | body | `string` | no | Optional footer text. |
| `button_display_text` | body | `string` | yes | Label for the URL button. |
| `button_url` | body | `string` | yes | The URL to open. |
