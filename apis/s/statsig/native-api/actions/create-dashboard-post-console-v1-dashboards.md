# Create Dashboard with Statsig

Creates a dashboard in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/dashboards`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Dashboard](https://docs.statsig.com/api-reference/dashboards/create-dashboard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `defaults` | body | `object` | no | Request body field. |
| `widgets` | body | `list` | no | Request body field. |
