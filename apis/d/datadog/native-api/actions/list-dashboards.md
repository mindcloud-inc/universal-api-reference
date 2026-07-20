# List Dashboards with Datadog

Retrieves dashboards from Datadog.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/dashboard`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [List Dashboards](https://docs.datadoghq.com/api/latest/dashboards/#get-all-dashboards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_shared` | query | `boolean` | no | Whether to return only shared dashboards. |
| `filter_deleted` | query | `boolean` | no | Whether to include deleted dashboards. |
| `count` | query | `number` | no | Maximum number of dashboards to return. |
| `start` | query | `number` | no | Starting offset for dashboard pagination. |
