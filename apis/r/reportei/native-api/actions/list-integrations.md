# List Integrations with Reportei

Retrieves integrations from Reportei.

## Endpoint

- **Method:** `GET`
- **Path:** `/integrations`
- **Base URL:** `https://app.reportei.com/api/v2`
- **Official documentation:** [List Integrations](https://developers.reportei.com#integracoes-endpoint-0)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `number` | no | Filtrar por projeto específico. |
| `name` | query | `string` | no | Filtrar pelo nome da integração. |
| `slug` | query | `string` | no | Filtrar pelo tipo de integração. |
