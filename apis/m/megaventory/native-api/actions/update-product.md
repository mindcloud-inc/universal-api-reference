# Update Product with Megaventory

Updates a product in Megaventory using a record action.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/ProductUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Update Product](https://api.megaventory.com/v2017a/json/metadata?op=ProductUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvProduct` | body | `object` | yes | Product payload to insert or update. |
| `mvRecordAction` | body | `string` | yes | Megaventory record action such as Insert or Update. |
| `forceSkuUpdateEvenIfUsedInDocuments` | body | `boolean` | no | Allow Megaventory to change the SKU even when documents already reference the product. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
