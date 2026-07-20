# <img src="https://images.mindcloud.co/apps/icons/square-space_1773072178168.png" alt="SquareSpace logo" width="28" height="28"> SquareSpace: Universal API

Squarespace Commerce API integration for reading and managing commerce data (orders, products, inventory, transactions) via the official Squarespace Commerce endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/squareSpace/latest
- **Category:** Commerce
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.squarespace.com
- **Vendor API docs:** https://developers.squarespace.com/commerce-apis/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Image Processing Status](actions/get-image-processing-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-image-processing-status?connectionId=$CONNECTION_ID&imageId=string&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Delete Product Image](actions/delete-product-image.md) | DELETE | Deletes a product image from Squarespace. |
| [Get Image Processing Status](actions/get-image-processing-status.md) | GET | Retrieves product image processing status from Squarespace. |
| [Reorder Product Image](actions/reorder-product-image.md) | PUT | Updates product image order in Squarespace. |
| [Update Product Image](actions/update-product-image.md) | PUT | Updates a product image in Squarespace. |
| [Upload Product Image](actions/upload-product-image.md) | POST | Uploads a product image to Squarespace. |

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [List Store Pages](actions/list-store-pages.md) | GET | Retrieves store pages from Squarespace. |

### Company Infos

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Basic Site Information](actions/retrieve-basic-site-information.md) | GET | Retrieves basic site information from Squarespace. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Profiles](actions/get-profiles.md) | GET | Retrieves customer profiles from Squarespace by ID. |
| [List Profiles](actions/list-profiles.md) | GET | Retrieves customer profiles from Squarespace. |

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [Adjust Stock Quantities](actions/adjust-stock-quantities.md) | PUT | Updates stock quantities in Squarespace. |
| [Get Inventory](actions/get-inventory.md) | GET | Retrieves inventory from Squarespace by ID. |
| [List Inventory](actions/list-inventory.md) | GET | Retrieves inventory from Squarespace. |

### Product Variants

| Action | Method | Description |
| --- | --- | --- |
| [Assign Product Image to Variant](actions/assign-product-image-to-variant.md) | PUT | Updates a product variant image in Squarespace. |
| [Create Product Variant](actions/create-product-variant.md) | POST | Creates a product variant in Squarespace. |
| [Delete Product Variant](actions/delete-product-variant.md) | DELETE | Deletes a product variant from Squarespace. |
| [Update Product Variant](actions/update-product-variant.md) | PUT | Updates a product variant in Squarespace. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a product in Squarespace. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes a product from Squarespace. |
| [Get Products](actions/get-products.md) | GET | Retrieves products from Squarespace by ID. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Squarespace. |
| [Update Product](actions/update-product.md) | PUT | Updates a product in Squarespace. |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates an order in Squarespace. |
| [Fulfill Order](actions/fulfill-order.md) | PUT | Updates order fulfillments in Squarespace. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Squarespace. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Squarespace. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Get Transactions](actions/get-transactions.md) | GET | Retrieves transactions from Squarespace by ID. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from Squarespace. |

