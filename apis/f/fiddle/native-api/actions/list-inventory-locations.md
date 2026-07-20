# List Inventory Locations with Fiddle

Retrieves inventory location records from Fiddle.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory-locations`
- **Base URL:** `https://fiddle.io/rest/api/v2`
- **Official documentation:** [List Inventory Locations](https://fiddle.io/rest/api/v2/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number |
| `size` | query | `number` | no | Page size |
| `query` | query | `string` | no | Inventory location search query |
| `inventoryLocationIds[]` | query | `array<string>` | no | Inventory location IDs |
| `siteIds[]` | query | `array<string>` | no | Site IDs |
| `sortBy` | query | `string` | no | Sort field |
| `sortDirection` | query | `string` | no | Sort direction |
