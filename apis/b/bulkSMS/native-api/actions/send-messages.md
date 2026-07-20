# Send Messages with BulkSMS

Sends one or more messages through BulkSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://api.bulksms.com/v1`
- **Official documentation:** [Send Messages](https://www.bulksms.com/developer/json/v1/#tag/message/POST/messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | Recipient phone number, recipient list, or group recipient details. |
| `body` | body | `string` | yes | SMS message content. |
| `from` | body | `string` | no | Optional sender ID or sender object. |
| `encoding` | body | `list` | no | Message encoding. Defaults to TEXT when omitted. Accepted values: `0`, `1`, `2`. |
| `routingGroup` | body | `list` | no | BulkSMS routing group. Accepted values: `0`, `1`, `2`. |
| `longMessageMaxParts` | body | `number` | no | Maximum number of parts for a concatenated message. |
| `userSuppliedId` | body | `string` | no | Client correlation value for sent messages, up to 20 characters. |
| `deliveryReports` | body | `list` | no | Delivery report mode requested from the delivering network. Accepted values: `0`, `1`, `2`. |
| `auto-unicode` | query | `boolean` | no | Automatically convert text to UNICODE when needed. |
| `schedule-date` | query | `date` | no | ISO-8601 date/time when BulkSMS should send the message. |
| `schedule-description` | query | `string` | no | Description for the scheduled message. |
| `deduplication-id` | query | `number` | no | Integer used by BulkSMS to avoid duplicate submissions. |
