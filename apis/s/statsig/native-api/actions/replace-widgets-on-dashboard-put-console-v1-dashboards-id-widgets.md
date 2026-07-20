# Replace Widgets on Dashboard with Statsig

Replaces widgets on dashboard in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/dashboards/{id}/widgets`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Replace Widgets on Dashboard](https://docs.statsig.com/api-reference/dashboards/replace-widgets-on-dashboard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `widgets` | body | `list` | yes | Request body field. |
| `defaults` | body | `object` | no | Request body field. |
| `max_cols` | body | `number` | no | Request body field. |
