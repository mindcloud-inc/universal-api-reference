# List Equipment Activity Entity Schedules with Grand Avenue Software

Retrieves equipment activity entity schedules from Grand Avenue Software.

## Endpoint

- **Method:** `GET`
- **Path:** `/EquipmentEntityActivitySchedules`
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
