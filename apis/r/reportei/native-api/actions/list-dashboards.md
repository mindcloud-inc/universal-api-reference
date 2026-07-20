# List Dashboards with Reportei

Retrieves dashboards from Reportei.

## Endpoint

- **Method:** `GET`
- **Path:** `/dashboards`
- **Base URL:** `https://app.reportei.com/api/v2`
- **Official documentation:** [List Dashboards](https://developers.reportei.com#dashboards-endpoint-0)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Filtrar por projeto específico. |
| `created_at` | query | `date` | no | Filtrar por data de criação. |
| `updated_at` | query | `date` | no | Filtrar por data de atualização. |
