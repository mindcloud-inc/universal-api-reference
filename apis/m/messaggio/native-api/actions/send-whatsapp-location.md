# Send WhatsApp Location with Messaggio

Creates a WhatsApp location message in Messaggio.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://msg.messaggio.com/api/v1`
- **Official documentation:** [Send WhatsApp Location](https://messaggio.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipientPhone` | body | `string` | yes | Recipient phone number in international format without a plus sign. |
| `senderCode` | body | `string` | yes | WhatsApp sender code from the Messaggio project. |
| `latitude` | body | `number` | yes | Location latitude. |
| `longitude` | body | `number` | yes | Location longitude. |
| `locationName` | body | `string` | yes | Location name. |
| `address` | body | `string` | yes | Location address. |
