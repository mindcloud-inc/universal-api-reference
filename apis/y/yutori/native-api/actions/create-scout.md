# Create Scout with Yutori

Creates a new scout in Yutori.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scouting/tasks`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Create Scout](https://docs.yutori.com/reference/scouts-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | What the scout should monitor in natural language. |
| `output_interval` | body | `number` | no | How often to run the scout, in seconds. |
| `start_timestamp` | body | `number` | no | Unix timestamp for when the scout should start. |
| `user_timezone` | body | `string` | no | Timezone used for scheduling context. |
| `user_location` | body | `string` | no | Coarse user location such as city, region, country. |
| `output_schema` | body | `object` | no | Optional JSON Schema for structured scout output. |
| `skip_email` | body | `boolean` | no | If true, skip email notifications. |
| `webhook_url` | body | `string` | no | Webhook URL to receive scout updates. |
| `webhook_format` | body | `string` | no | Webhook payload format. |
| `is_public` | body | `boolean` | no | Whether the scout is publicly accessible. |
