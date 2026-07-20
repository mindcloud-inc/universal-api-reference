# Update Product Category with Megaventory

Updates a product category in Megaventory using a record action.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/ProductCategoryUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Update Product Category](https://api.megaventory.com/v2017a/json/metadata?op=ProductCategoryUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvProductCategory` | body | `object` | yes | Product category payload to insert, update, or delete. |
| `mvRecordAction` | body | `string` | yes | Megaventory record action such as Insert, Update, or Delete. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
