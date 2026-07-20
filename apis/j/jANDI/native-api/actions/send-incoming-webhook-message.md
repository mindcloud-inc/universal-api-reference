# Send Incoming Webhook Message with JANDI

## Endpoint

- **Method:** `POST`
- **Path:** `{incomingWebhookUrl}`
- **Base URL:** `https://wh.jandi.com`
- **Official documentation:** [Send Incoming Webhook Message](https://support.jandi.com/en/articles/Receiving-Incoming-Webhooks-in-JANDI-56bacd47)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | The main JANDI message text. This is the only required field. |
| `connectColor` | body | `string` | no | Optional hex color for the attachment bar. |
| `connectInfo[]` | body | `array<object>` | no | Optional attachment items to include below the message body. |
