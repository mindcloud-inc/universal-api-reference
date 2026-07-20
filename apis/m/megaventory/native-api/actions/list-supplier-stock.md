# List Supplier Stock with Megaventory

Retrieves supplier stock records from Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/SupplierStockGet`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [List Supplier Stock](https://api.megaventory.com/v2017a/json/metadata?op=SupplierStockGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filters` | body | `list<object>` | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | body | `number` | no | Maximum number of rows Megaventory should return. |
| `ProductSKU` | body | `string` | no | Filter results to a specific product SKU. |
| `ProductCategoryID` | body | `number` | no | Filter results to a specific product category ID. |
| `ProductMainSupplierID` | body | `number` | no | Filter results to a specific main supplier ID. |
| `includeReferencedObjects` | body | `boolean` | no | Ask Megaventory to include related records in the response. |
