# List Timeline Events with Reportei

Retrieves timeline events from Reportei.

## Endpoint

- **Method:** `GET`
- **Path:** `/timeline-events`
- **Base URL:** `https://app.reportei.com/api/v2`
- **Official documentation:** [List Timeline Events](https://developers.reportei.com#timeline-endpoint-0)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Filtrar por projeto. |
| `report_id` | query | `number` | no | Filtrar por relatório. |
| `date` | query | `date` | no | Filtrar por data. |
