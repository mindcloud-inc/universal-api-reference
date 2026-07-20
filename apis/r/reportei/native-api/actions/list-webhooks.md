# List Webhooks with Reportei

Retrieves webhooks from Reportei.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhooks`
- **Base URL:** `https://app.reportei.com/api/v2`
- **Official documentation:** [List Webhooks](https://developers.reportei.com#webhooks-endpoint-0)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Filtrar por projeto. |
| `event_type` | query | `string` | no | Filtrar por tipo de evento. |
| `source` | query | `string` | no | Filtrar por source. |
| `status` | query | `number` | no | Filtrar por status. |
