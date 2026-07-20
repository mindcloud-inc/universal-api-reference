# List Downtimes with Datadog

Retrieves downtimes from Datadog.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/downtime`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [List Downtimes](https://docs.datadoghq.com/api/latest/downtimes/#get-all-downtimes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `current_only` | query | `boolean` | no | Return only currently active downtimes. |
| `include` | query | `string` | no | Additional related resources to include. |
| `page[limit]` | query | `number` | no | Maximum number of downtimes to return. |
| `page[offset]` | query | `number` | no | Pagination offset for downtimes. |
