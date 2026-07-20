# Send WhatsApp Free-form Reply with TopMessage

Creates a WhatsApp free-form reply in TopMessage.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages`
- **Base URL:** `https://api.topmessage.com`
- **Official documentation:** [Send WhatsApp Free-form Reply](https://topmessage.com/documentation-api/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.from` | body | `string` | yes | The sender name or virtual number the message appears to come from. |
| `data.to[]` | body | `array<string>` | yes | One or more recipient phone numbers in international format. |
| `data.text` | body | `string` | yes | The free-form WhatsApp reply content to send. |
