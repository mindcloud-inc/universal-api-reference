# List Product Categories with Megaventory

Retrieves product category records from Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/ProductCategoryGet`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [List Product Categories](https://api.megaventory.com/v2017a/json/metadata?op=ProductCategoryGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filters` | body | `list<object>` | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | body | `number` | no | Maximum number of rows Megaventory should return. |
| `showDeleted` | body | `boolean` | no | Include archived product categories. |
