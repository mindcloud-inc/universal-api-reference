# <img src="https://images.mindcloud.co/apps/icons/paddle_1775768292725.png" alt="Paddle logo" width="28" height="28"> Paddle: Universal API

Manage payments, subscriptions, and billing data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/paddle/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.paddle.com/
- **Vendor API docs:** https://developer.paddle.com/api-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Event Types](actions/list-event-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paddle/latest/actions/list-event-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Paddle. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Paddle. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from Paddle. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Paddle. |

### Discounts

| Action | Method | Description |
| --- | --- | --- |
| [Create Discount](actions/create-discount.md) | POST | Creates a new discount in Paddle. |
| [Get Discount](actions/get-discount.md) | GET | Retrieves a discount from Paddle. |
| [List Discounts](actions/list-discounts.md) | GET | Retrieves a list of discounts from Paddle. |
| [Update Discount](actions/update-discount.md) | PUT | Updates an existing discount in Paddle. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Event Types](actions/list-event-types.md) | GET | Retrieves a list of event types from Paddle. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Create Notification Setting](actions/create-notification-setting.md) | POST | Creates a notification setting in Paddle. |
| [List Notification Settings](actions/list-notification-settings.md) | GET | Retrieves a list of notification settings from Paddle. |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves a list of notifications from Paddle. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [Create Price](actions/create-price.md) | POST | Creates a new price in Paddle. |
| [Get Price](actions/get-price.md) | GET | Retrieves a price from Paddle. |
| [List Prices](actions/list-prices.md) | GET | Retrieves a list of prices from Paddle. |
| [Preview Prices](actions/preview-prices.md) | GET | Retrieves a pricing preview from Paddle. |
| [Update Price](actions/update-price.md) | PUT | Updates an existing price in Paddle. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Paddle. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Paddle. |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from Paddle. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Paddle. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Portal Session](actions/create-customer-portal-session.md) | POST | Creates a customer portal session in Paddle. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT | Cancels an existing subscription in Paddle. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from Paddle. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves a list of subscriptions from Paddle. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in Paddle. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | POST | Creates a new transaction in Paddle. |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Paddle. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves a list of transactions from Paddle. |
| [Update Transaction](actions/update-transaction.md) | PUT | Updates an existing transaction in Paddle. |

