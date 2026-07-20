# Create Campaign with Mailrelay

Creates a new campaign in Mailrelay.

## Endpoint

- **Method:** `POST`
- **Path:** `campaigns`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Create Campaign](https://apidocs.mailrelay.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_ids[]` | body | `array<number>` | no | Group IDs when target is `groups`. |
| `html` | body | `string` | yes | Campaign HTML content. |
| `segment_id` | body | `number` | no | Segment ID when target is `segment`. |
| `sender_id` | body | `number` | yes | Sender ID for the campaign. |
| `subject` | body | `string` | yes | Campaign subject. |
| `target` | body | `list` | yes | Who the campaign should be sent to. Accepted values: `0`, `1`. |
