# Send WhatsApp Template with Messaggio

Creates a WhatsApp template message in Messaggio.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://msg.messaggio.com/api/v1`
- **Official documentation:** [Send WhatsApp Template](https://messaggio.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipientPhone` | body | `string` | yes | Recipient phone number in international format without a plus sign. |
| `senderCode` | body | `string` | yes | WhatsApp sender code from the Messaggio project. |
| `templateId` | body | `string` | yes | Approved WhatsApp template identifier in Messaggio. |
| `language` | body | `string` | yes | Template language code, such as en. |
| `bodyParam1` | body | `string` | no | First optional template body parameter. |
| `bodyParam2` | body | `string` | no | Second optional template body parameter. |
| `urlParameter` | body | `string` | no | Optional dynamic URL parameter for a template URL button. |
