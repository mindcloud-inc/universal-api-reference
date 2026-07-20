# Set Topic Notification Level with Discourse

Updates a topic's notification level in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/t/:id/notifications.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Set Topic Notification Level](https://docs.discourse.org/#tag/Topics/operation/setNotificationLevel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Topic id to update notification settings for. |
| `notification_level` | body | `string` | yes | Notification level: 0 muted, 1 regular, 2 tracking, 3 watching. Accepted values: `0`, `1`, `2`, `3`. |
