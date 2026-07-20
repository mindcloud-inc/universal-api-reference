# Update Campaign with Mailrelay

Updates an existing campaign in Mailrelay.

## Endpoint

- **Method:** `PATCH`
- **Path:** `campaigns/:id`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Update Campaign](https://apidocs.mailrelay.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_ids[]` | body | `array<number>` | no | Updated group IDs when target is `groups`. |
| `html` | body | `string` | no | Updated campaign HTML content. |
| `id` | path | `number` | yes | The Mailrelay campaign ID. |
| `segment_id` | body | `number` | no | Updated segment ID when target is `segment`. |
| `sender_id` | body | `number` | no | Updated sender ID for the campaign. |
| `subject` | body | `string` | no | Updated campaign subject. |
| `target` | body | `list` | no | Updated campaign target. Accepted values: `0`, `1`. |
