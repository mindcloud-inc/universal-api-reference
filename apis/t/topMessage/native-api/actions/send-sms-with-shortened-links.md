# Send SMS With Shortened Links with TopMessage

Creates an SMS message with shortened links in TopMessage.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages`
- **Base URL:** `https://api.topmessage.com`
- **Official documentation:** [Send SMS With Shortened Links](https://topmessage.com/documentation-api/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.from` | body | `string` | yes | The sender name or virtual number the message appears to come from. |
| `data.to[]` | body | `array<string>` | yes | One or more recipient phone numbers in international format. |
| `data.text` | body | `string` | yes | The SMS content to send, including any HTTPS URLs to shorten. |
