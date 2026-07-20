# List Product Suppliers with Megaventory

Retrieves product supplier links from Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/ProductSupplierGet`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [List Product Suppliers](https://api.megaventory.com/v2017a/json/metadata?op=ProductSupplierGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filters` | body | `list<object>` | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | body | `number` | no | Maximum number of rows Megaventory should return. |
| `IncludeReferencedObjects` | body | `boolean` | no | Ask Megaventory to include related records in the response. |
