# Send Campaign with Mailrelay

Sends a Mailrelay campaign to its selected audience.

## Endpoint

- **Method:** `POST`
- **Path:** `campaigns/:id/send_all`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Send Campaign](https://apidocs.mailrelay.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callback_url` | body | `string` | no | Webhook URL to notify after the campaign is sent. |
| `group_ids[]` | body | `array<number>` | no | Group IDs when target is `groups`. |
| `id` | path | `number` | yes | The Mailrelay campaign ID. |
| `scheduled_at` | body | `string` | no | UTC send time in `YYYY-MM-DD HH:MM:SS` format. |
| `segment_id` | body | `number` | no | Segment ID when target is `segment`. |
| `target` | body | `list` | yes | Who the campaign should be sent to. Accepted values: `0`, `1`. |
