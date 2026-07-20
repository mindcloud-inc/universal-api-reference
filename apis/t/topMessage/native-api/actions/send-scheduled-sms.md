# Send Scheduled SMS with TopMessage

Creates a scheduled SMS message in TopMessage.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages`
- **Base URL:** `https://api.topmessage.com`
- **Official documentation:** [Send Scheduled SMS](https://topmessage.com/documentation-api/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.from` | body | `string` | yes | The sender name or virtual number the message appears to come from. |
| `data.to[]` | body | `array<string>` | yes | One or more recipient phone numbers in international format. |
| `data.text` | body | `string` | yes | The SMS content to send later. |
| `data.schedule` | body | `date` | yes | The UTC ISO-8601 time when TopMessage should send the message. |
