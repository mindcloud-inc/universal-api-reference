# Send Message with Pushover

## Endpoint

- **Method:** `POST`
- **Path:** `/messages.json`
- **Base URL:** `https://api.pushover.net/1`
- **Official documentation:** [Send Message](https://pushover.net/api#messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | query | `string` | yes | User key or group key to send the message to. |
| `message` | query | `string` | yes | Message body to push through Pushover. |
| `device` | query | `string` | no | Optional device name to target instead of all active devices. |
| `title` | query | `string` | no | Optional message title. |
| `priority` | query | `number` | no | Message priority from -2 to 2. |
| `sound` | query | `string` | no | Sound name to override the recipient's default tone. |
| `url` | query | `string` | no | Supplementary URL to show with the message. |
| `url_title` | query | `string` | no | Optional label shown for the supplementary URL. |
| `timestamp` | query | `number` | no | Unix timestamp to display instead of the receipt time. |
| `ttl` | query | `number` | no | Seconds before the message expires and is deleted automatically. |
| `html` | query | `number` | no | Set to 1 to enable HTML formatting. |
| `monospace` | query | `number` | no | Set to 1 to enable monospace formatting. |
| `retry` | query | `number` | no | Seconds between retries for emergency-priority messages. |
| `expire` | query | `number` | no | Maximum retry window in seconds for emergency-priority messages. |
| `callback` | query | `string` | no | Public callback URL that Pushover calls when an emergency message is acknowledged. |
| `tags` | query | `string` | no | Comma-separated tags stored with an emergency receipt for later cancellation. |
| `attachment_base64` | query | `string` | no | Base64-encoded image attachment. |
| `attachment_type` | query | `string` | no | MIME type for the Base64 attachment. |
