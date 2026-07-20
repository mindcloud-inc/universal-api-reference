# Create Website with condoo

Creates a new website in condoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/websites`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [Create Website](https://trk.condoo.systems/en/api-documentation/websites)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_exclusion_is_enabled` | body | `boolean` | no | Whether bot exclusion is enabled. |
| `domain_id` | body | `number` | no | Optional domain ID to associate with the website. |
| `email_reports_is_enabled` | body | `boolean` | no | Whether email reports are enabled. |
| `events_children_is_enabled` | body | `boolean` | no | Whether child event tracking is enabled. |
| `excluded_ips` | body | `string` | no | Optional excluded IP list. |
| `host` | body | `string` | yes | Required website host. |
| `is_enabled` | body | `boolean` | no | Optional enabled toggle. |
| `name` | body | `string` | yes | Required website name. |
| `outbound_clicks_is_enabled` | body | `boolean` | no | Optional outbound-click tracking toggle. |
| `public_statistics_is_enabled` | body | `boolean` | no | Optional public statistics toggle. |
| `public_statistics_password` | body | `string` | no | Optional password when public statistics are enabled. |
| `query_parameters_tracking_is_enabled` | body | `boolean` | no | Whether query parameter tracking is enabled. |
| `scheme` | body | `string` | yes | Required URL scheme. Allowed values: http, https. |
| `sessions_replays_hide_text_selector` | body | `string` | no | Optional selector for text hidden in session replays. |
| `sessions_replays_is_enabled` | body | `boolean` | no | Whether session replays are enabled. |
| `tracking_type` | body | `string` | no | Optional tracking type. Allowed values: normal, lightweight. |
