# Delete Message with MojoTxt

Deletes a message from MojoTxt.

## Endpoint

- **Method:** `POST`
- **Path:** `/:phoneNumber/messages/delete/:messageId`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [Delete Message](https://app.mojotxt.com/api/docs/v1/messages-delete.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The message identifier to delete. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
