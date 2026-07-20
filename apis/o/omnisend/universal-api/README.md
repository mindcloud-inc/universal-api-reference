# <img src="https://images.mindcloud.co/apps/icons/omnisend_1774537145891.png" alt="Omnisend logo" width="28" height="28"> Omnisend: Universal API

Omnisend helps ecommerce teams manage email and SMS marketing, customer data sync, orders, carts, products, and custom events from one platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/omnisend/latest
- **Category:** Marketing
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.omnisend.com
- **Vendor API docs:** https://api-docs.omnisend.com/reference/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch](actions/create-batch.md) | POST | Creates a batch request in Omnisend. |

### Carts

| Action | Method | Description |
| --- | --- | --- |
| [Get Cart](actions/get-cart.md) | GET | Retrieves a cart from Omnisend. |
| [List Carts](actions/list-carts.md) | GET | Retrieves carts from Omnisend. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new product category in Omnisend. |
| [List Categories](actions/list-categories.md) | GET | Retrieves product categories from Omnisend. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing product category in Omnisend. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in Omnisend, or updates an existing one. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Omnisend. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Omnisend. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Omnisend. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Events](actions/list-custom-events.md) | GET | Retrieves custom events from Omnisend. |
| [Trigger Custom Event](actions/trigger-custom-event.md) | POST | Triggers a custom event in Omnisend. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Omnisend. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Omnisend. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Omnisend. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Omnisend. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Omnisend. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Omnisend. |
| [Replace Product](actions/replace-product.md) | PUT | Replaces an existing product in Omnisend. |

