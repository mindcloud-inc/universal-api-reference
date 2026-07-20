# <img src="https://images.mindcloud.co/apps/icons/copperx-icon_1775658056761.png" alt="Copperx logo" width="28" height="28"> Copperx: Universal API

Copperx API for managing organizations, payment settings, customers, invoices, payment links, checkout sessions, products, prices, tax rates, subscriptions, webhooks, and related payment operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/copperx/latest
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.copperx.io
- **Vendor API docs:** https://copperx.readme.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Assets](actions/list-assets.md) | GET | Retrieves all asset records from Copperx. |

### Chain

| Action | Method | Description |
| --- | --- | --- |
| [List Chains](actions/list-chains.md) | GET | Retrieves all chain records from Copperx. |

### Checkout Session

| Action | Method | Description |
| --- | --- | --- |
| [Get Checkout Session](actions/get-checkout-session.md) | GET | Retrieves a checkout session from Copperx. |
| [List Checkout Sessions](actions/list-checkout-sessions.md) | GET | Retrieves all checkout sessions from Copperx. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves customer record details from Copperx. |
| [List Customers](actions/list-customers.md) | GET | Retrieves all customer records from Copperx. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Duplicate Invoice](actions/duplicate-invoice.md) | PUT | Duplicates an existing invoice in Copperx. |
| [Finalize Invoice](actions/finalize-invoice.md) | PUT | Finalizes an existing invoice in Copperx. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves invoice record details from Copperx. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves all invoice records from Copperx. |
| [Send Invoice](actions/send-invoice.md) | PUT | Sends an invoice and finalizes it if needed in Copperx. |
| [Void Invoice](actions/void-invoice.md) | PUT | Voids an existing invoice in Copperx. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Info](actions/get-organization-info.md) | GET | Retrieves organization record details from Copperx. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Activate Payment Link](actions/activate-payment-link.md) | PUT | Activates a payment link in Copperx. |
| [Deactivate Payment Link](actions/deactivate-payment-link.md) | PUT | Deactivates a payment link in Copperx. |
| [Get Payment Link](actions/get-payment-link.md) | GET | Retrieves a payment link from Copperx. |
| [Get Payment Setting](actions/get-payment-setting.md) | GET | Retrieves organization payment settings from Copperx. |
| [List Payment Links](actions/list-payment-links.md) | GET | Retrieves all payment links from Copperx. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get Price](actions/get-price.md) | GET | Retrieves price record details from Copperx. |
| [Get Price Constants](actions/get-price-constants.md) | GET | Retrieves pricing constant values from Copperx. |
| [List Prices](actions/list-prices.md) | GET | Retrieves all price records from Copperx. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Activate Product](actions/activate-product.md) | PUT | Activates an existing product in Copperx. |
| [Deactivate Product](actions/deactivate-product.md) | PUT | Deactivates an existing product in Copperx. |
| [Get Product](actions/get-product.md) | GET | Retrieves product record details from Copperx. |
| [List Products](actions/list-products.md) | GET | Retrieves all product records from Copperx. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves subscription record details from Copperx. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves all subscription records from Copperx. |

### Tax Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Tax Rate](actions/get-tax-rate.md) | GET | Retrieves a tax rate from Copperx. |
| [List Tax Rates](actions/list-tax-rates.md) | GET | Retrieves all tax rates from Copperx. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves all transaction records from Copperx. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Copperx. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Endpoint](actions/get-webhook-endpoint.md) | GET | Retrieves a webhook endpoint from Copperx. |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | GET | Retrieves all webhook endpoints from Copperx. |

### Withdrawal Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Withdrawal Address](actions/get-withdrawal-address.md) | GET | Retrieves a withdrawal address from Copperx. |
| [List Withdrawal Addresses](actions/list-withdrawal-addresses.md) | GET | Retrieves all withdrawal addresses from Copperx. |

