# <img src="https://images.mindcloud.co/apps/icons/goody_1774282011079.png" alt="Goody logo" width="28" height="28"> Goody: Universal API

Goody Commerce API wrapper for catalog, pricing, order batch, order, payment method, and webhook operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goody/latest
- **Category:** Commerce
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ongoody.com
- **Vendor API docs:** https://developer.ongoody.com/commerce-api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goody/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Card

| Action | Method | Description |
| --- | --- | --- |
| [List Cards](actions/list-cards.md) | GET | Retrieves active cards from Goody. |

### Current User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Goody. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | PUT | Cancels an order in Goody. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Goody. |
| [List Order Batch Orders](actions/list-order-batch-orders.md) | GET | Retrieves orders for an order batch in Goody. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Goody. |
| [Update Order Expiration](actions/update-order-expiration.md) | PUT | Updates an order's expiration in Goody. |

### Order Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Order Activities](actions/list-order-activities.md) | GET | Retrieves order activities from Goody. |

### Order Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create Order Batch](actions/create-order-batch.md) | POST | Creates a new order batch in Goody. |
| [Get Order Batch](actions/get-order-batch.md) | GET | Retrieves an order batch from Goody. |
| [List Order Batches](actions/list-order-batches.md) | GET | Retrieves order batches from Goody. |

### Order Batch Price

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Order Batch Price](actions/calculate-order-batch-price.md) | GET | Calculates an order batch price in Goody. |

### Order Batch Recipient

| Action | Method | Description |
| --- | --- | --- |
| [List Order Batch Recipients](actions/list-order-batch-recipients.md) | GET | Retrieves recipients for an order batch in Goody. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [Create Commerce User Payment Method](actions/create-commerce-user-payment-method.md) | POST | Creates a commerce user payment method in Goody. |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves payment methods from Goody. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a specific product from Goody. |
| [List Products](actions/list-products.md) | GET | Retrieves active products from Goody. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook endpoint in Goody. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook endpoint from Goody. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Goody. |

