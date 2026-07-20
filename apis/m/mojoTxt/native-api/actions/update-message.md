# Update Message with MojoTxt

Updates a message in MojoTxt.

## Endpoint

- **Method:** `POST`
- **Path:** `/:phoneNumber/messages/update/:messageId`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [Update Message](https://app.mojotxt.com/api/docs/v1/messages-update.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Lists[]` | body | `array<number>` | no | One or more list IDs to send the message to. |
| `Media` | body | `string` | no | Media URL required when sending an MMS. |
| `Message` | body | `string` | no | The updated message body. |
| `messageId` | path | `string` | yes | The message identifier to update. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
| `PublishTime` | body | `number` | no | UNIX timestamp for when the message should be sent. |
| `ScheduleType` | body | `string` | no | S for a specific send time or R for a time relative to subscription. |
| `SendAfter` | body | `number` | no | Delay before sending a relative message. |
| `SendAfterUnit` | body | `string` | no | Unit for SendAfter: hour, day, week, month, or year. |
| `Type` | body | `string` | no | SMS or MMS. |
| `URL` | body | `string` | no | Tracking URL to append to the outgoing message. |
