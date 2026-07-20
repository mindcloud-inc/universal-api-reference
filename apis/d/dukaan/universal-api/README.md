# <img src="https://images.mindcloud.co/apps/icons/png-clipart-dukaan-logo-tech-companies-thumbnail_1776268417531.png" alt="Dukaan logo" width="28" height="28"> Dukaan: Universal API

Dukaan Public APIs for building custom apps, plugins, workflows, and store operations across products, orders, customers, discounts, and inventory.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dukaan/latest
- **Category:** Commerce
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mydukaan.io
- **Vendor API docs:** https://documenter.getpostman.com/view/25389466/2s9Yynk3f7

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0&storeUuid=your-store-uuid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Category](actions/create-product-category.md) | POST | Creates a new product category in Dukaan. |
| [List Product Categories](actions/list-product-categories.md) | GET | Retrieves product categories from Dukaan. |
| [Search Product Categories](actions/search-product-categories.md) | GET | Finds product categories in Dukaan by search query. |
| [Update Product Category](actions/update-product-category.md) | PUT | Updates an existing product category in Dukaan. |

### Coupons

| Action | Method | Description |
| --- | --- | --- |
| [Create Discount](actions/create-discount.md) | POST | Creates a new discount in Dukaan. |
| [List Discounts](actions/list-discounts.md) | GET | Retrieves discounts from Dukaan. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Dukaan. |
| [Get Customer Details](actions/get-customer-details.md) | GET | Retrieves customer details from Dukaan. |
| [List Store Audience](actions/list-store-audience.md) | GET | Retrieves store audience records from Dukaan. |
| [Update Customer Notes](actions/update-customer-notes.md) | PUT | Updates customer notes in Dukaan. |

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Products](actions/list-inventory-products.md) | GET | Retrieves inventory products from Dukaan. |
| [Update Inventory](actions/update-inventory.md) | PUT | Updates inventory quantities in Dukaan. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Dukaan. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Dukaan. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Dukaan. |
| [Search Orders](actions/search-orders.md) | GET | Finds orders in Dukaan by search query. |
| [Update Order Status](actions/update-order-status.md) | PUT | Updates an order status in Dukaan. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Dukaan. |
| [Create Product With Variants](actions/create-product-with-variants.md) | POST | Creates a new product with variants in Dukaan. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from a Dukaan store. |
| [List Products](actions/list-products.md) | GET | Retrieves products from a Dukaan store. |
| [List Products By Category](actions/list-products-by-category.md) | GET | Retrieves products in a Dukaan category. |
| [Search Products](actions/search-products.md) | GET | Finds products in Dukaan by search query. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Dukaan. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Add Customer Tag](actions/add-customer-tag.md) | POST | Adds a tag to a customer in Dukaan. |
| [Create Customer Tag Definition](actions/create-customer-tag-definition.md) | POST | Creates a new customer tag definition in Dukaan. |

### Warehouses

| Action | Method | Description |
| --- | --- | --- |
| [Create Warehouse](actions/create-warehouse.md) | POST | Creates a new warehouse in Dukaan. |
| [List Warehouses](actions/list-warehouses.md) | GET | Retrieves warehouses from Dukaan. |
| [Update Warehouse](actions/update-warehouse.md) | PUT | Updates an existing warehouse in Dukaan. |

