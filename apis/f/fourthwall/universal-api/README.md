# <img src="https://images.mindcloud.co/apps/icons/fourthwall_1773779492048.png" alt="Fourthwall logo" width="28" height="28"> Fourthwall: Universal API

Manage Fourthwall products, orders, promotions, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fourthwall/latest
- **Category:** Commerce
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fourthwall.com
- **Vendor API docs:** https://docs.fourthwall.com/guides/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Shop](actions/get-current-shop.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/get-current-shop?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Collections](actions/list-collections.md) | GET | Retrieves a paginated list of collections from Fourthwall. |

### External Order

| Action | Method | Description |
| --- | --- | --- |
| [Get External Order](actions/get-external-order.md) | GET | Retrieves an external order from Fourthwall by source and ID. |
| [List External Orders](actions/list-external-orders.md) | GET | Retrieves external orders from Fourthwall with optional filters. |
| [Validate External Order](actions/validate-external-order.md) | POST | Validates an external order in Fourthwall before creation. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Fourthwall by ID. |
| [Get Order By Friendly ID](actions/get-order-by-friendly-id.md) | GET | Retrieves an order from Fourthwall by friendly ID. |
| [List Orders](actions/list-orders.md) | GET | Retrieves a paginated list of orders from Fourthwall. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Fourthwall by ID. |
| [List Products](actions/list-products.md) | GET | Retrieves a paginated list of products from Fourthwall. |
| [Update Product Availability](actions/update-product-availability.md) | PUT | Updates a product's storefront availability in Fourthwall. |

### Product Inventory

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Inventory](actions/get-product-inventory.md) | GET | Retrieves product inventory from Fourthwall by product ID. |

### Promotion

| Action | Method | Description |
| --- | --- | --- |
| [Create Promotion](actions/create-promotion.md) | POST | Creates a new promotion in Fourthwall. |
| [Get Promotion](actions/get-promotion.md) | GET | Retrieves a promotion from Fourthwall by ID. |
| [List Promotions](actions/list-promotions.md) | GET | Retrieves a list of promotions from Fourthwall. |

### Shop

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Shop](actions/get-current-shop.md) | GET | Retrieves the current shop from Fourthwall. |

### Shop Contact Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Shop Contact Info](actions/get-shop-contact-info.md) | GET | Retrieves current shop contact info from Fourthwall. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Fourthwall. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Fourthwall. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from Fourthwall. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Fourthwall. |

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Events](actions/list-webhook-events.md) | GET | Retrieves webhook events from Fourthwall with optional type filtering. |

