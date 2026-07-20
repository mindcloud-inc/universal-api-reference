# Send VKontakte Text with Messaggio

Creates a VKontakte text message in Messaggio.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://msg.messaggio.com/api/v1`
- **Official documentation:** [Send VKontakte Text](https://messaggio.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipientPhone` | body | `string` | yes | Recipient phone number in international format without a plus sign. |
| `senderCode` | body | `string` | yes | VK sender code from the Messaggio project. |
| `messageText` | body | `string` | yes | VK message text. |
