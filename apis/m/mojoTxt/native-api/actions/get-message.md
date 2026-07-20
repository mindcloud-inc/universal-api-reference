# Get Message with MojoTxt

Retrieves a message from MojoTxt.

## Endpoint

- **Method:** `GET`
- **Path:** `/:phoneNumber/messages/get/:messageId`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [Get Message](https://app.mojotxt.com/api/docs/v1/messages-get.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The message identifier to retrieve. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
