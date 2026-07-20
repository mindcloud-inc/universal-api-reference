# List Work Orders with Fiddle

Retrieves work order records from Fiddle.

## Endpoint

- **Method:** `GET`
- **Path:** `/work-orders`
- **Base URL:** `https://fiddle.io/rest/api/v2`
- **Official documentation:** [List Work Orders](https://fiddle.io/rest/api/v2/docs/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number |
| `size` | query | `number` | no | Page size |
| `query` | query | `string` | no | Work order search query |
| `status` | query | `string` | no | Status selector |
| `statuses` | query | `string` | no | Statuses selector |
| `customerId` | query | `string` | no | Customer ID selector |
| `inventoryItemId` | query | `string` | no | Inventory item ID selector |
| `archived` | query | `boolean` | no | Archived selector |
| `sortBy` | query | `string` | no | Sort field |
| `sortDirection` | query | `string` | no | Sort direction |
