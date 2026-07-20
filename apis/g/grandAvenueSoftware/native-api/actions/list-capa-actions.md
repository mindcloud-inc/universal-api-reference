# List Capa Actions with Grand Avenue Software

Retrieves CAPA actions from Grand Avenue Software.

## Endpoint

- **Method:** `GET`
- **Path:** `/CapaActions`
- **Base URL:** `{baseUrl}`
- **API:** REST

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | e.g. `UpdatedTimestamp > 2025-12-18T00:00:00.000Z` |
| `$select` | query | `list<string>` | no | Send multiple values as a string. |
| `$expand` | query | `list<string>` | no | Send multiple values as a string. |
| `$count` | query | `boolean` | no | Use count to return the total number of results. |
