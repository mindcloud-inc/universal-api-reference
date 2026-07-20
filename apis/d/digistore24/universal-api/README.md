# <img src="https://images.mindcloud.co/apps/icons/digistore24_1773241963560.png" alt="Digistore24 logo" width="28" height="28"> Digistore24: Universal API

Manage products, purchases, and affiliates with Digistore24

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/digistore24/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.digistore24.com/en
- **Vendor API docs:** https://dev.digistore24.com/hc/en-us/articles/38492246374673-API-reference-A-Z

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Buy Url

| Action | Method | Description |
| --- | --- | --- |
| [Create Buy URL](actions/create-buy-url.md) | POST | Creates a customized buy URL in Digistore24. |
| [List Buy URLs](actions/list-buy-urls.md) | GET | Retrieves a list of buy URLs from Digistore24. |

### Buyer

| Action | Method | Description |
| --- | --- | --- |
| [Update Buyer](actions/update-buyer.md) | PUT | Updates an existing buyer in Digistore24. |

### Commission

| Action | Method | Description |
| --- | --- | --- |
| [List Commissions](actions/list-commissions.md) | GET | Retrieves a list of commission amounts from Digistore24. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices for a Digistore24 purchase. |

### Payment Plan

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Plan](actions/create-payment-plan.md) | POST | Creates a new payment plan in Digistore24. |
| [List Payment Plans](actions/list-payment-plans.md) | GET | Retrieves payment plans for a Digistore24 product. |
| [Update Payment Plan](actions/update-payment-plan.md) | PUT | Updates an existing payment plan in Digistore24. |

### Payout

| Action | Method | Description |
| --- | --- | --- |
| [List Payouts](actions/list-payouts.md) | GET | Retrieves payout credit notes from Digistore24. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Digistore24. |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from Digistore24. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Digistore24. |

### Product Group

| Action | Method | Description |
| --- | --- | --- |
| [List Product Groups](actions/list-product-groups.md) | GET | Retrieves a list of product groups from Digistore24. |
| [Update Product Group](actions/update-product-group.md) | PUT | Updates an existing product group in Digistore24. |

### Purchase

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase](actions/get-purchase.md) | GET | Retrieves detailed purchase data from Digistore24. |
| [List Purchases](actions/list-purchases.md) | GET | Retrieves a list of purchases from Digistore24. |
| [Refund Partially](actions/refund-partially.md) | PUT | Partially refunds a payment in Digistore24 while keeping the order status. |
| [Refund Purchase](actions/refund-purchase.md) | PUT | Refunds all refundable payments for a Digistore24 purchase. |
| [Update Purchase](actions/update-purchase.md) | PUT | Updates an existing purchase in Digistore24. |

### Rebilling

| Action | Method | Description |
| --- | --- | --- |
| [Start Rebilling](actions/start-rebilling.md) | PUT | Resumes rebilling for a Digistore24 purchase. |
| [Stop Rebilling](actions/stop-rebilling.md) | PUT | Stops rebilling for a Digistore24 purchase. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves payments, returns, and chargebacks from Digistore24. |
| [Refund Transaction](actions/refund-transaction.md) | PUT | Refunds a payment transaction in Digistore24. |

### Voucher

| Action | Method | Description |
| --- | --- | --- |
| [List Vouchers](actions/list-vouchers.md) | GET | Retrieves a list of voucher codes from Digistore24. |

