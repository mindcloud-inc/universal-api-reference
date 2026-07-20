# Send a message through the Zapper integration with Chatvolt AI

Sends an a message through the Zapper integration through Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/zapper/instances/{id}/message`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Send a message through the Zapper integration](https://docs.chatvolt.ai/api-reference/endpoint/zapper/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Zapper instance ID (externalId of the ServiceProvider of type 'zapper'). |
| `message` | body | `string` | no | Textual content of the message. |
| `contactPhone` | body | `string` | no | Recipient's number. |
| `attachments[]` | body | `array<object>` | no | Optional list of attachments to be sent. |
