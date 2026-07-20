# List Current Inventory with Katana

Lists current inventory records in Katana.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [List Current Inventory](https://developer.katanamrp.com/reference/list-current-inventory)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location_id` | query | `number` | no | Filters inventories by a valid location id |
| `variant_id[]` | query | `array<number>` | no | Filters inventories by valid variant ids |
| `include_archived` | query | `boolean` | no | Includes archived inventories |
| `extend[]` | query | `array<string>` | no | Array of objects that need to be added to the response |
