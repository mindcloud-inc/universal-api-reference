# Send Message with Mobile Text Alerts

Creates a message in Mobile Text Alerts.

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://api.mobile-text-alerts.com/v3`
- **Official documentation:** [Send Message](https://developers.mobile-text-alerts.com/api-reference/send#post-send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscribers` | body | `string` | yes | Comma-separated phone numbers or emails to send the message to. |
| `message` | body | `string` | no | Message content to send. |
| `templateId` | body | `number` | no | Controlled template ID to use instead of freeform message content. |
| `image` | body | `string` | no | Optional attachment URL for MMS sends. |
| `header` | body | `string` | no | Optional text inserted before the message body. |
| `footer` | body | `string` | no | Optional text appended after the message body. |
| `scheduledDate` | body | `string` | no | Optional scheduled send time in ISO 8601 format like 20250306T193000-0000. |
