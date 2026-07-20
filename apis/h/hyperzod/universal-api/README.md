# <img src="https://images.mindcloud.co/apps/icons/hyperzod_1774900813368.png" alt="Hyperzod logo" width="28" height="28"> Hyperzod: Universal API

Hyperzod: Manage merchants, orders, products, and hyperlocal delivery

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hyperzod/latest
- **Category:** Commerce
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hyperzod.com/
- **Vendor API docs:** https://app.archbee.com/public/PREVIEW-TSX59B-ftH01Uoa0aU550

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Order Status](actions/list-order-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/list-order-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Create Address](actions/create-address.md) | POST | Creates a new address in Hyperzod. |
| [Delete Address](actions/delete-address.md) | DELETE | Deletes an existing address from Hyperzod. |
| [Fetch Address](actions/fetch-address.md) | GET | Retrieves an address from Hyperzod. |
| [Update Address](actions/update-address.md) | PUT | Updates an existing address in Hyperzod. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Hyperzod. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from Hyperzod. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from Hyperzod. |

### Merchant

| Action | Method | Description |
| --- | --- | --- |
| [Create Merchant](actions/create-merchant.md) | POST | Creates a new merchant in Hyperzod. |
| [Delete Merchant](actions/delete-merchant.md) | DELETE | Deletes an existing merchant from Hyperzod. |
| [List Merchants](actions/list-merchants.md) | GET | Retrieves a list of merchants from Hyperzod. |
| [Update Merchant](actions/update-merchant.md) | PUT | Updates an existing merchant in Hyperzod. |

### Merchant Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Merchant Category](actions/create-merchant-category.md) | POST | Creates a new merchant category in Hyperzod. |
| [Delete Merchant Category](actions/delete-merchant-category.md) | DELETE | Deletes an existing merchant category from Hyperzod. |
| [List Merchant Categories](actions/list-merchant-categories.md) | GET | Retrieves a list of merchant categories from Hyperzod. |
| [Update Merchant Category](actions/update-merchant-category.md) | PUT | Updates an existing merchant category in Hyperzod. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Hyperzod. |
| [Create Order Note](actions/create-order-note.md) | POST | Creates a new note on an order in Hyperzod. |
| [List Order Commissions](actions/list-order-commissions.md) | GET | Retrieves a list of order commissions from Hyperzod. |
| [List Orders](actions/list-orders.md) | GET | Retrieves a list of orders from Hyperzod. |
| [List Scheduled Orders](actions/list-scheduled-orders.md) | GET | Retrieves a list of scheduled orders from Hyperzod. |
| [Retrieve Order](actions/retrieve-order.md) | GET | Retrieves an order from Hyperzod. |
| [Retrieve Order Scheduling Slots](actions/retrieve-order-scheduling-slots.md) | GET | Retrieves order scheduling slots from Hyperzod. |
| [Retrieve Order Stats](actions/retrieve-order-stats.md) | GET | Retrieves order statistics from Hyperzod by delivery date. |
| [Update Order Status](actions/update-order-status.md) | PUT | Updates an order's status in Hyperzod. |

### Order Status

| Action | Method | Description |
| --- | --- | --- |
| [List Order Status](actions/list-order-status.md) | GET | Retrieves available order statuses from Hyperzod. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Product Inventory](actions/bulk-update-product-inventory.md) | PUT | Updates product inventory counts in bulk in Hyperzod. |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Hyperzod. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Hyperzod. |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from Hyperzod. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Hyperzod. |

### Product Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Category](actions/create-product-category.md) | POST | Creates a new product category in Hyperzod. |
| [Delete Product Category](actions/delete-product-category.md) | DELETE | Deletes an existing product category from Hyperzod. |
| [List Product Categories](actions/list-product-categories.md) | GET | Retrieves a list of product categories from Hyperzod. |
| [Retrieve Product Category](actions/retrieve-product-category.md) | GET | Retrieves a product category from Hyperzod. |
| [Update Product Category](actions/update-product-category.md) | PUT | Updates an existing product category in Hyperzod. |

### Product Label

| Action | Method | Description |
| --- | --- | --- |
| [Create Product Label](actions/create-product-label.md) | POST | Creates a new product label in Hyperzod. |
| [Delete Product Label](actions/delete-product-label.md) | DELETE | Deletes an existing product label from Hyperzod. |
| [List Product Labels](actions/list-product-labels.md) | GET | Retrieves a list of product labels from Hyperzod. |
| [Retrieve Product Label](actions/retrieve-product-label.md) | GET | Retrieves a product label from Hyperzod. |
| [Update Product Label](actions/update-product-label.md) | PUT | Updates an existing product label in Hyperzod. |

