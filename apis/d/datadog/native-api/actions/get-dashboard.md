# Get Dashboard with Datadog

Retrieves a dashboard from Datadog.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/dashboard/:dashboard_id`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Get Dashboard](https://docs.datadoghq.com/api/latest/dashboards/#get-a-dashboard)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dashboard_id` | path | `string` | yes | The ID of the dashboard. |
