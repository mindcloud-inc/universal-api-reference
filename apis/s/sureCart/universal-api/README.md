# <img src="https://images.mindcloud.co/apps/icons/id43j8vly-x-logos_1774890183617.png" alt="SureCart logo" width="28" height="28"> SureCart: Universal API

Sell products, manage subscriptions, process orders, and operate a commerce storefront in SureCart.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sureCart/latest
- **Category:** Commerce
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://surecart.com
- **Vendor API docs:** https://developer.surecart.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Account](actions/retrieve-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Account](actions/retrieve-account.md) | GET |  |
| [Update Account](actions/update-account.md) | PUT |  |

### Checkout

| Action | Method | Description |
| --- | --- | --- |
| [Create Checkout](actions/create-checkout.md) | POST |  |
| [List Checkouts](actions/list-checkouts.md) | GET |  |
| [Retrieve Checkout](actions/retrieve-checkout.md) | GET |  |
| [Update Checkout](actions/update-checkout.md) | PUT |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Delete Customer](actions/delete-customer.md) | DELETE |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Retrieve Customer](actions/retrieve-customer.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET |  |
| [Retrieve Order](actions/retrieve-order.md) | GET |  |

### Price

| Action | Method | Description |
| --- | --- | --- |
| [Create Price](actions/create-price.md) | POST |  |
| [Delete Price](actions/delete-price.md) | DELETE |  |
| [List Prices](actions/list-prices.md) | GET |  |
| [Retrieve Price](actions/retrieve-price.md) | GET |  |
| [Update Price](actions/update-price.md) | PUT |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Delete Product](actions/delete-product.md) | DELETE |  |
| [List Products](actions/list-products.md) | GET |  |
| [Retrieve Product](actions/retrieve-product.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Purchase

| Action | Method | Description |
| --- | --- | --- |
| [List Purchases](actions/list-purchases.md) | GET |  |
| [Retrieve Purchase](actions/retrieve-purchase.md) | GET |  |
| [Revoke Purchase](actions/revoke-purchase.md) | PUT |  |
| [Update Purchase](actions/update-purchase.md) | PUT |  |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [Create Refund](actions/create-refund.md) | POST |  |
| [List Refunds](actions/list-refunds.md) | GET |  |
| [Retrieve Refund](actions/retrieve-refund.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Cancel/Pause Subscription](actions/cancel-pause-subscription.md) | PUT |  |
| [Create Subscription](actions/create-subscription.md) | POST |  |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |
| [Retrieve Subscription](actions/retrieve-subscription.md) | GET |  |
| [Update Subscription](actions/update-subscription.md) | PUT |  |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Endpoint](actions/create-webhook-endpoint.md) | POST |  |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | GET |  |
| [Retrieve Webhook Endpoint](actions/retrieve-webhook-endpoint.md) | GET |  |
| [Test Webhook Endpoint](actions/test-webhook-endpoint.md) | PUT |  |
| [Update Webhook Endpoint](actions/update-webhook-endpoint.md) | PUT |  |

