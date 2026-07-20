# <img src="https://images.mindcloud.co/apps/icons/woo-commerce_1773670558737.png" alt="WooCommerce logo" width="28" height="28"> WooCommerce: Universal API

Manage WooCommerce products, orders, customers, and store settings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wooCommerce/latest
- **Category:** Commerce
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://woocommerce.com
- **Vendor API docs:** https://woocommerce.github.io/woocommerce-rest-api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooCommerce/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Coupon

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupon](actions/create-coupon.md) | POST | Creates a new coupon in WooCommerce. |
| [Delete Coupon](actions/delete-coupon.md) | DELETE | Deletes an existing coupon from WooCommerce. |
| [List Coupons](actions/list-coupons.md) | GET | Retrieves coupons from WooCommerce. |
| [Retrieve Coupon](actions/retrieve-coupon.md) | GET | Retrieves a coupon from WooCommerce. |
| [Update Coupon](actions/update-coupon.md) | PUT | Updates an existing coupon in WooCommerce. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in WooCommerce. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from WooCommerce. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from WooCommerce. |
| [Retrieve Customer](actions/retrieve-customer.md) | GET | Retrieves a customer from WooCommerce. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in WooCommerce. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in WooCommerce. |
| [Create Order Note](actions/create-order-note.md) | PUT | Creates an order note in WooCommerce. |
| [Delete Order](actions/delete-order.md) | DELETE | Deletes an existing order from WooCommerce. |
| [Get Order Note](actions/get-order-note.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from WooCommerce. |
| [Retrieve Order](actions/retrieve-order.md) | GET | Retrieves an order from WooCommerce. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in WooCommerce. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in WooCommerce. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from WooCommerce. |
| [Duplicate Product](actions/duplicate-product.md) | POST | Creates a duplicate product in WooCommerce. |
| [List Products](actions/list-products.md) | GET | Retrieves products from WooCommerce. |
| [Retrieve Product](actions/retrieve-product.md) | GET | Retrieves a product from WooCommerce. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in WooCommerce. |

### Product Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Category](actions/create-product-category.md) | POST | Creates a new product category in WooCommerce. |
| [List Product Categories](actions/list-product-categories.md) | GET | Retrieves product categories from WooCommerce. |
| [Retrieve Product Category](actions/retrieve-product-category.md) | GET | Retrieves a product category from WooCommerce. |

