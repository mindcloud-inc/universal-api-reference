# Send Viber Text + Image + Button with Messaggio

Creates a Viber image message with a button in Messaggio.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://msg.messaggio.com/api/v1`
- **Official documentation:** [Send Viber Text + Image + Button](https://messaggio.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipientPhone` | body | `string` | yes | Recipient phone number in international format without a plus sign. |
| `senderCode` | body | `string` | yes | Viber sender code from the Messaggio project. |
| `messageLabel` | body | `string` | yes | Viber message label. Use promotion or transaction. |
| `messageText` | body | `string` | yes | Viber message text. |
| `imageUrl` | body | `string` | yes | Public URL of the image to send through Viber. |
| `buttonText` | body | `string` | yes | Viber button caption. |
| `buttonUrl` | body | `string` | yes | URL to open when the Viber button is pressed. |
