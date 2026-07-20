# Send Message by Channel with Chatvolt AI

Sends a message by channel through Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversation/message/{type}/{value}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Send Message by Channel](https://docs.chatvolt.ai/api-reference/endpoint/conversation/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Type of conversation identifier. It can be "conversationId" for the conversation ID, "phone" for the phone number, or "email" for the email address. |
| `value` | path | `string` | yes | Value corresponding to the identifier type specified in "type". |
| `message` | body | `string` | yes | Content of the message to be sent. |
| `agentId` | body | `string` | no | (Optional) Agent ID, in cuid format. |
| `channel` | body | `string` | no | (Optional) Channel used to send the message. |
| `attachments[]` | body | `array<object>` | no | (Optional) List of attachments to be sent. |
| `visitorId` | body | `string` | no | (Optional) Visitor ID, if applicable. |
| `contactId` | body | `string` | no | (Optional) Contact ID, if applicable. |
