# Update Product Supplier with Megaventory

Updates a product supplier link in Megaventory using a record action.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/ProductSupplierUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Update Product Supplier](https://api.megaventory.com/v2017a/json/metadata?op=ProductSupplierUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvProductSupplierUpdate` | body | `object` | yes | Product and supplier relationship payload to insert, update, or delete. |
| `mvRecordAction` | body | `string` | yes | Megaventory record action such as Insert, Update, or Delete. |
