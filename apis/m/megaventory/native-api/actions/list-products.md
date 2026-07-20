# List Products with Megaventory

Retrieves existing product records from Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/ProductGet`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [List Products](https://api.megaventory.com/v2017a/json/metadata?op=ProductGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filters` | body | `list<object>` | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | body | `number` | no | Maximum number of rows Megaventory should return. |
| `ProductID` | body | `number` | no | Filter results to a specific Megaventory product ID. |
| `ProductSKU` | body | `string` | no | Filter results to a specific product SKU. |
| `ProductCategoryID` | body | `number` | no | Filter results to a specific product category ID. |
| `ProductMainSupplierID` | body | `number` | no | Filter results to a specific main supplier ID. |
| `includeReferencedObjects` | body | `boolean` | no | Ask Megaventory to include related records in the response. |
| `showDeleted` | body | `boolean` | no | Include archived product records. |
