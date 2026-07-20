# List Inventory Levels with Megaventory

Retrieves inventory level records from Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/InventoryLocationStockGet`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [List Inventory Levels](https://api.megaventory.com/v2017a/json/metadata?op=InventoryLocationStockGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filters` | body | `list<object>` | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | body | `number` | no | Maximum number of rows Megaventory should return. |
| `ProductID` | body | `number` | no | Filter results to a specific Megaventory product ID. |
| `ProductSKU` | body | `string` | no | Filter results to a specific product SKU. |
| `ProductCategoryID` | body | `number` | no | Filter results to a specific product category ID. |
| `InventoryLocationID` | body | `number` | no | Filter results to a specific inventory location ID. |
| `ProductMainSupplierID` | body | `number` | no | Filter results to a specific main supplier ID. |
| `includeReferencedObjects` | body | `boolean` | no | Ask Megaventory to include related records in the response. |
| `ShowOnlyProductsWithPositiveQty` | body | `boolean` | no | Limit results to products with positive stock. |
| `ShowOnlyProductsThanNeedToBeOrdered` | body | `boolean` | no | Limit results to products that need reordering. |
| `showDeleted` | body | `boolean` | no | Include archived stock records. |
