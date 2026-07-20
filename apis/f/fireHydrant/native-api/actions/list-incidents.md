# List Incidents with FireHydrant

Retrieves incidents from FireHydrant.

## Endpoint

- **Method:** `GET`
- **Path:** `/incidents`
- **Base URL:** `https://api.firehydrant.io/v1`
- **Official documentation:** [List Incidents](https://docs.firehydrant.com/reference/list_incidents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search incident name, summary, and description. |
| `name` | query | `string` | no | Filter incidents by name. |
| `services` | query | `string` | no | Comma-separated service IDs to filter incidents by impacted services. Send multiple values as a string separated by `,`. |
| `teams` | query | `string` | no | Comma-separated team IDs to filter incidents by teams. Send multiple values as a string separated by `,`. |
| `severities` | query | `string` | no | Comma-separated severities to filter incidents. Send multiple values as a string separated by `,`. |
| `start_date` | query | `date` | no | Filter incidents that started on or after this timestamp. |
| `end_date` | query | `date` | no | Filter incidents that started on or before this timestamp. |
| `status` | query | `string` | no | Filter by incident status. |
