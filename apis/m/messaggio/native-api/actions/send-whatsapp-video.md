# Send WhatsApp Video with Messaggio

Creates a WhatsApp video message in Messaggio.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://msg.messaggio.com/api/v1`
- **Official documentation:** [Send WhatsApp Video](https://messaggio.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipientPhone` | body | `string` | yes | Recipient phone number in international format without a plus sign. |
| `senderCode` | body | `string` | yes | WhatsApp sender code from the Messaggio project. |
| `mediaUrl` | body | `string` | yes | Public URL of the video file to send through WhatsApp. |
