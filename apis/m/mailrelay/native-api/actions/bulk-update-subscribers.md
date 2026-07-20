# Bulk Update Subscribers with Mailrelay

Updates multiple subscriber records in Mailrelay.

## Endpoint

- **Method:** `PATCH`
- **Path:** `subscribers/bulk_update`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Bulk Update Subscribers](https://apidocs.mailrelay.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `all_subscribers` | body | `boolean` | no | Update all subscribers instead of a specific list. |
| `bulk_action` | body | `list` | yes | Bulk subscriber update action. Accepted values: `0`. |
| `callback_url` | body | `string` | no | Webhook URL to receive the bulk update task ID when processing finishes. |
| `group_id` | body | `number` | no | Group ID used by the bulk update action. |
| `subscriber_ids[]` | body | `array<number>` | no | Subscriber IDs affected by the bulk update action. |
