# Send Viber Text with Messaggio

Creates a Viber text message in Messaggio.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://msg.messaggio.com/api/v1`
- **Official documentation:** [Send Viber Text](https://messaggio.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipientPhone` | body | `string` | yes | Recipient phone number in international format without a plus sign. |
| `senderCode` | body | `string` | yes | Viber sender code from the Messaggio project. |
| `messageLabel` | body | `string` | yes | Viber message label. Use promotion or transaction. |
| `messageText` | body | `string` | yes | Viber message text. Maximum length: 1000. |
