# List Monitors with Datadog

Retrieves monitors from Datadog.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/monitor`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [List Monitors](https://docs.datadoghq.com/api/latest/monitors/#get-all-monitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_states` | query | `string` | no | Comma-separated monitor group states to include: all, alert, warn, or no data. |
| `id_offset` | query | `number` | no | Starting monitor ID for offset-style pagination through large monitor sets. |
| `monitor_tags` | query | `string` | no | Comma-separated service or custom monitor tags to filter the monitor list. |
| `name` | query | `string` | no | Filter monitors by monitor name. |
| `page` | query | `number` | no | Page number to start paginating from. |
| `page_size` | query | `number` | no | Number of monitors to return per page. |
| `tags` | query | `string` | no | Comma-separated scope tags to filter the monitor list. |
| `with_downtimes` | query | `boolean` | no | Include current active downtimes for each returned monitor. |
