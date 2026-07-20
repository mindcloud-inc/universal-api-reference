# Send SMS Template Message with TopMessage

Creates an SMS template message in TopMessage.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages`
- **Base URL:** `https://api.topmessage.com`
- **Official documentation:** [Send SMS Template Message](https://topmessage.com/documentation-api/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.from` | body | `string` | yes | The sender name or virtual number the message appears to come from. |
| `data.to[]` | body | `array<string>` | yes | One or more recipient phone numbers in international format. |
| `data.template_id` | body | `string` | yes | The existing TopMessage template identifier to send. |
