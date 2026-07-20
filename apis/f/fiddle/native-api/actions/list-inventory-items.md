# List Inventory Items with Fiddle

Retrieves inventory item records from Fiddle.

## Endpoint

- **Method:** `GET`
- **Path:** `/inventory-items`
- **Base URL:** `https://fiddle.io/rest/api/v2`
- **Official documentation:** [List Inventory Items](https://fiddle.io/rest/api/v2/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number |
| `size` | query | `number` | no | Page size |
| `query` | query | `string` | no | Inventory item search query |
| `status` | query | `string` | no | Status selector |
| `inventoryTypeId` | query | `string` | no | Inventory type ID selector |
| `supplierId` | query | `string` | no | Supplier ID selector |
| `inventoryTypeIds[]` | query | `array<string>` | no | Inventory type ID list |
| `exclude[]` | query | `array<string>` | no | Inventory item IDs to exclude |
| `exactMatch` | query | `boolean` | no | Whether to exact-match the query |
| `hideEmpty` | query | `boolean` | no | Hide empty inventory items |
| `inventoryLocations[]` | query | `array<string>` | no | Inventory location IDs |
| `hasMasterFormula` | query | `boolean` | no | Whether the item has a master formula |
| `hasMasterBillOfMaterial` | query | `boolean` | no | Whether the item has a master bill of material |
| `startDate` | query | `date` | no | Start date |
| `endDate` | query | `date` | no | End date |
| `showOnlyNonZeroTotalValue` | query | `boolean` | no | Show only items with non-zero total value |
| `archived` | query | `boolean` | no | Archived selector |
| `excludeStatuses[]` | query | `array<string>` | no | Statuses to exclude |
| `sortBy` | query | `string` | no | Sort field |
| `sortDirection` | query | `string` | no | Sort direction |
