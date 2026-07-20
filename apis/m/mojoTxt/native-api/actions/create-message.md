# Create Message with MojoTxt

Creates a message in MojoTxt.

## Endpoint

- **Method:** `POST`
- **Path:** `/:phoneNumber/messages/add`
- **Base URL:** `https://app.mojotxt.com/api/v1`
- **Official documentation:** [Create Message](https://app.mojotxt.com/api/docs/v1/messages-add.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Lists[]` | body | `array<number>` | yes | One or more list IDs to send the message to. |
| `Media` | body | `string` | no | Media URL required when sending an MMS. |
| `Message` | body | `string` | yes | The message body to send. |
| `phoneNumber` | path | `string` | yes | The MojoTxt phone number in international format, like +17792533748. |
| `PublishTime` | body | `number` | no | UNIX timestamp for when the message should be sent. |
| `ScheduleType` | body | `string` | no | S for a specific send time or R for a time relative to subscription. |
| `SendAfter` | body | `number` | no | Delay before sending a relative message. |
| `SendAfterUnit` | body | `string` | no | Unit for SendAfter: hour, day, week, month, or year. |
| `Type` | body | `string` | no | The message type, either SMS or MMS. |
| `URL` | body | `string` | no | Tracking URL to append to the outgoing message. |
