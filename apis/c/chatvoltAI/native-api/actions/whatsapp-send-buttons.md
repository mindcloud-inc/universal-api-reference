# Send Buttons with Chatvolt AI

Sends interactive buttons through Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/interactive/send-buttons`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Send Buttons](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/send-buttons)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | The ID of the agent sending the message. |
| `conversationId` | body | `string` | yes | The ID of the conversation. |
| `header_text` | body | `string` | no | Optional header text. |
| `body_text` | body | `string` | yes | The main message body. |
| `footer_text` | body | `string` | no | Optional footer text. |
| `button_1_id` | body | `string` | yes | ID for the first button. |
| `button_1_title` | body | `string` | yes | Label for the first button. |
| `button_2_id` | body | `string` | no | ID for the second button. |
| `button_2_title` | body | `string` | no | Label for the second button. |
| `button_3_id` | body | `string` | no | ID for the third button. |
| `button_3_title` | body | `string` | no | Label for the third button. |
