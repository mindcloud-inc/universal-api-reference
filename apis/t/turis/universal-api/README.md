# <img src="https://images.mindcloud.co/apps/icons/turis_1774648647673.png" alt="Turis logo" width="28" height="28"> Turis: Universal API

Manage wholesale orders, products, buyers, and companies in Turis

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/turis/latest
- **Category:** Commerce
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://turis.app
- **Vendor API docs:** https://documenter.getpostman.com/view/16452985/TzkyP1Er

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Orders](actions/list-orders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Buyer

| Action | Method | Description |
| --- | --- | --- |
| [Create Buyer](actions/create-buyer.md) | POST | Creates a new buyer in Turis. |
| [Get Buyer](actions/get-buyer.md) | GET | Retrieves a buyer from Turis. |
| [List Buyers](actions/list-buyers.md) | GET | Retrieves buyers from Turis. |
| [Update Buyer](actions/update-buyer.md) | PUT | Updates an existing buyer in Turis. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in Turis. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Turis. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Turis. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from Turis. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Turis. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Turis. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves currencies from Turis. |

### Delivery

| Action | Method | Description |
| --- | --- | --- |
| [Create Delivery](actions/create-delivery.md) | POST | Creates a new delivery in Turis. |
| [List Deliveries](actions/list-deliveries.md) | GET | Retrieves deliveries from Turis. |
| [Update Delivery](actions/update-delivery.md) | PUT | Updates an existing delivery in Turis. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Add Products to Order](actions/add-products-to-order.md) | PUT | Adds products to a Turis order. |
| [Create Order](actions/create-order.md) | POST | Creates a new order in Turis. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Turis. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Turis. |
| [List Orders by Status](actions/list-orders-by-status.md) | GET | Retrieves orders in Turis by status. |
| [List Orders Updated Between Dates](actions/list-orders-updated-between-dates.md) | GET | Retrieves Turis orders updated between two dates. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in Turis. |
| [Update Order Items](actions/update-order-items.md) | PUT | Updates items in a Turis order. |
| [Update Order Tags](actions/update-order-tags.md) | PUT | Updates tags on a Turis order. |

### Order Status

| Action | Method | Description |
| --- | --- | --- |
| [List Order Statuses](actions/list-order-statuses.md) | GET | Retrieves order statuses from Turis. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Turis. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Turis. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Turis. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Turis. |
| [Update Product Inventory](actions/update-product-inventory.md) | PUT | Updates product inventory in Turis. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tags](actions/create-tags.md) | POST | Creates one or more tags in Turis. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Turis. |

