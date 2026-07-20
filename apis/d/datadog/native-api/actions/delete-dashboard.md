# Delete Dashboard with Datadog

Deletes an existing dashboard from Datadog.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/dashboard/:dashboard_id`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Delete Dashboard](https://docs.datadoghq.com/api/latest/dashboards/#delete-a-dashboard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dashboard_id` | path | `string` | yes | The ID of the dashboard. |
