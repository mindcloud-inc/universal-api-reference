# Send Telegram Media + Button with Messaggio

Creates a Telegram media message with a button in Messaggio.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://msg.messaggio.com/api/v1`
- **Official documentation:** [Send Telegram Media + Button](https://messaggio.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipientPhone` | body | `string` | yes | Recipient phone number in international format without a plus sign. |
| `botToken` | body | `string` | yes | Telegram bot token configured as the sender code in Messaggio. |
| `mediaType` | body | `string` | yes | Telegram media type: image, video, or document. |
| `fileUrl` | body | `string` | yes | Public URL of the Telegram media file. |
| `buttonText` | body | `string` | yes | Telegram button caption. |
| `buttonUrl` | body | `string` | yes | URL to open when the Telegram button is pressed. |
