# Get Product with Checkout Page

Retrieves a product from Checkout Page.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/products/:productId`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Get Product](https://checkoutpage.com/docs/api/v1/products/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | yes | Unique identifier. Must be in BSON ObjectId format. |
