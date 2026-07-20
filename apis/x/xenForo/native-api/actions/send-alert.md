# Send Alert with XenForo

Sends an alert to a user in XenForo.

## Endpoint

- **Method:** `POST`
- **Path:** `/alerts/`
- **Base URL:** `{baseUrl}/2310/api`
- **Official documentation:** [Send Alert](https://docs.xenforo.com/api/post-alerts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to_user_id` | body | `number` | yes | ID of the user who will receive the alert. |
| `alert` | body | `string` | yes | Alert text. Use {link} where the link should be inserted. |
| `from_user_id` | body | `number` | no | Optional user ID to send the alert from. Use 0 for an anonymous alert. |
| `link_url` | body | `string` | no | Optional URL opened when the alert is clicked. |
| `link_title` | body | `string` | no | Optional link text shown with the alert. |
