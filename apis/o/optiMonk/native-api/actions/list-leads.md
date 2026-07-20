# List Leads with OptiMonk

Retrieves leads from OptiMonk.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads/`
- **Base URL:** `https://api.optimonk.com/v1`
- **Official documentation:** [List Leads](https://api.optimonk.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval` | query | `string` | no | Predefined reporting interval. |
| `from` | query | `string` | no | Start date or datetime for a custom interval. |
| `to` | query | `string` | no | End date or datetime for a custom interval. |
| `page` | query | `number` | no | Pagination index. Starts at 1. |
