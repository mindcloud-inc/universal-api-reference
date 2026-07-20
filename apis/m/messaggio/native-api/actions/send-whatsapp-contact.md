# Send WhatsApp Contact with Messaggio

Creates a WhatsApp contact message in Messaggio.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://msg.messaggio.com/api/v1`
- **Official documentation:** [Send WhatsApp Contact](https://messaggio.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipientPhone` | body | `string` | yes | Recipient phone number in international format without a plus sign. |
| `senderCode` | body | `string` | yes | WhatsApp sender code from the Messaggio project. |
| `firstName` | body | `string` | yes | Contact first name included in the shared WhatsApp contact card. |
| `formattedName` | body | `string` | yes | Formatted contact name shown in WhatsApp. |
| `contactPhone` | body | `string` | yes | Phone number included in the shared WhatsApp contact card. |
