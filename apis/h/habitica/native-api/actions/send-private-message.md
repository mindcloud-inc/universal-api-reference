# Send Private Message with Habitica

Sends a private message to a Habitica member.

## Endpoint

- **Method:** `POST`
- **Path:** `/members/send-private-message`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Send Private Message](https://habitica.com/apidoc/#api-Member-SendPrivateMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `toUserId` | body | `string` | yes | The Habitica member ID that should receive the private message. |
| `message` | body | `string` | yes | The message text to send. |
