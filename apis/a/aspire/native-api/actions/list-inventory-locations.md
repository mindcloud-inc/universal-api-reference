# List Inventory Locations with Aspire

Retrieves inventory locations from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `InventoryLocations`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Inventory Locations](https://guide.youraspire.com/apidocs/inventorylocations-6)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
