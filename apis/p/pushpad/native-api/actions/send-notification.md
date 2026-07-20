# Send Notification with Pushpad

Sends a web push notification with Pushpad.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/notifications`
- **Base URL:** `https://pushpad.xyz/api/v1`
- **Official documentation:** [Send Notification](https://pushpad.xyz/docs/rest_api#notifications_api_docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actions[]` | body | `array<object>` | no | Send multiple values as a array. |
| `badge_url` | body | `string` | no | — |
| `body` | body | `string` | yes | — |
| `custom_data` | body | `string` | no | — |
| `custom_metrics[]` | body | `array<string>` | no | Send multiple values as a array. |
| `icon_url` | body | `string` | no | — |
| `image_url` | body | `string` | no | — |
| `project_id` | path | `number` | yes | — |
| `require_interaction` | body | `boolean` | no | — |
| `send_at` | body | `date` | no | — |
| `silent` | body | `boolean` | no | — |
| `starred` | body | `boolean` | no | — |
| `tags[]` | body | `array<string>` | no | Send multiple values as a array. |
| `target_url` | body | `string` | no | — |
| `title` | body | `string` | no | — |
| `ttl` | body | `number` | no | — |
| `uids[]` | body | `array<string>` | no | Send multiple values as a array. |
| `urgent` | body | `boolean` | no | — |
