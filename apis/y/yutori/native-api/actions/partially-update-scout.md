# Partially Update Scout with Yutori

Updates specific fields of an existing scout in Yutori.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/scouting/tasks/:scout_id`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Partially Update Scout](https://docs.yutori.com/reference/scouts-patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scout_id` | path | `string` | yes | The scout UUID. |
| `query` | body | `string` | no | Updated scout prompt. |
| `output_interval` | body | `number` | no | Updated output interval in seconds. |
| `user_timezone` | body | `string` | no | Updated timezone. |
| `user_location` | body | `string` | no | Updated coarse location. |
| `is_public` | body | `boolean` | no | Whether the scout is publicly accessible. |
| `skip_email` | body | `boolean` | no | If true, email notifications are skipped. |
| `webhook_url` | body | `string` | no | Webhook URL to receive updates. |
| `webhook_format` | body | `string` | no | Webhook payload format. |
