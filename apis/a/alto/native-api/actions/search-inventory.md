# Search Inventory with Alto

Finds inventory items in Alto by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory/search`
- **Base URL:** `https://api.alto.zoopladev.co.uk`
- **Official documentation:** [Search Inventory](https://developers.vebraalto.com/api)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search text for inventory items. |
| `recordType` | query | `string` | no | Inventory record type filter. |
| `archived` | query | `boolean` | no | Whether to search archived inventory records. |
