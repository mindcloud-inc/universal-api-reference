# List Sales Orders with SOS Inventory

Retrieves sales orders from SOS Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/salesorder`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [List Sales Orders](https://developer.sosinventory.com/apidoc/SalesOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `string` | no | Return archived yes/no sales orders. |
| `channel` | query | `string` | no | Filter by channel name. |
| `location` | query | `string` | no | Filter by location name. |
| `orderStage` | query | `string` | no | Filter by order stage name. |
| `query` | query | `string` | no | Filter by number, comment, customer PO, or customer name. |
| `status` | query | `string` | no | Filter by open or closed status. |
