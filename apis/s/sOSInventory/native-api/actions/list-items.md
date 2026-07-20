# List Items with SOS Inventory

Retrieves items from SOS Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/item`
- **Base URL:** `https://api.sosinventory.com`
- **Official documentation:** [List Items](https://developer.sosinventory.com/apidoc/Item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `string` | no | Return archived yes/no items. |
| `category` | query | `string` | no | Filter items by category name. |
| `location` | query | `string` | no | Filter items by location name. |
| `query` | query | `string` | no | Filter by matches on full name, description, notes, barcode, sku, vendor part number, or tags. |
| `sku` | query | `string` | no | Search for a single SKU. |
| `tags` | query | `string` | no | Filter by a comma-separated list of tags. |
| `type` | query | `string` | no | Filter by item type. |
