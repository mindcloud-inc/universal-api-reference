# Send Verification SMS with TopMessage

Creates a verification SMS message in TopMessage.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages`
- **Base URL:** `https://api.topmessage.com`
- **Official documentation:** [Send Verification SMS](https://topmessage.com/documentation-api/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.from` | body | `string` | yes | The sender name or virtual number the message appears to come from. |
| `data.to[]` | body | `array<string>` | yes | One or more recipient phone numbers in international format. |
| `data.text` | body | `string` | yes | Include the {code} placeholder so TopMessage replaces it with an auto-generated verification code. |
