# Update Product Client with Megaventory

Updates a product client link in Megaventory using a record action.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/ProductClientUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Update Product Client](https://api.megaventory.com/v2017a/json/metadata?op=ProductClientUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvProductClientUpdate` | body | `object` | yes | Product and client relationship payload to insert, update, or delete. |
| `mvRecordAction` | body | `string` | yes | Megaventory record action such as Insert, Update, or Delete. |
