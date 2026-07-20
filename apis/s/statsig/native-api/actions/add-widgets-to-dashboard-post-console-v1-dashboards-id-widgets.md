# Add Widgets to Dashboard with Statsig

Adds widgets to dashboard in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/dashboards/{id}/widgets`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Add Widgets to Dashboard](https://docs.statsig.com/api-reference/dashboards/add-widgets-to-dashboard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `widgets` | body | `list` | yes | Request body field. |
| `defaults` | body | `object` | no | Request body field. |
| `max_cols` | body | `number` | no | Request body field. |
