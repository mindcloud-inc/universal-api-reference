# <img src="https://images.mindcloud.co/apps/icons/images_1773522889310.png" alt="Paystack logo" width="28" height="28"> Paystack: Universal API

Paystack: Accept payments, manage customers, subscriptions, products, payment pages, and payment requests

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/paystack/latest
- **Category:** Commerce
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://paystack.com/
- **Vendor API docs:** https://paystack.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Transactions](actions/list-transactions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Bank

| Action | Method | Description |
| --- | --- | --- |
| [List Banks](actions/list-banks.md) | GET |  |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Fetch Customer](actions/fetch-customer.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |
| [Whitelist/Blacklist Customer](actions/whitelist-blacklist-customer.md) | PUT |  |

### Payment Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST |  |
| [Fetch Page](actions/fetch-page.md) | GET |  |
| [List Pages](actions/list-pages.md) | GET |  |

### Payment Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Request](actions/create-payment-request.md) | POST |  |
| [Fetch Payment Request](actions/fetch-payment-request.md) | GET |  |
| [List Payment Requests](actions/list-payment-requests.md) | GET |  |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Create Plan](actions/create-plan.md) | POST |  |
| [Fetch Plan](actions/fetch-plan.md) | GET |  |
| [List Plans](actions/list-plans.md) | GET |  |
| [Update Plan](actions/update-plan.md) | PUT |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Fetch Product](actions/fetch-product.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST |  |
| [Fetch Subscription](actions/fetch-subscription.md) | GET |  |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Transaction](actions/fetch-transaction.md) | GET |  |
| [Initialize Transaction](actions/initialize-transaction.md) | POST |  |
| [List Transactions](actions/list-transactions.md) | GET |  |
| [Verify Transaction](actions/verify-transaction.md) | GET |  |

### Transaction Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Transactions](actions/export-transactions.md) | GET |  |

### Transaction Totals Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction Totals](actions/get-transaction-totals.md) | GET |  |

