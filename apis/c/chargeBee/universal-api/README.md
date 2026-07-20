# <img src="https://images.mindcloud.co/apps/icons/favicon-v2_1754337795745.png" alt="ChargeBee logo" width="28" height="28"> ChargeBee: Universal API

Chargebee is a subscription billing and revenue management platform for managing customers, subscriptions, invoices, credit notes, payments, events, products, and catalog data through Chargebee's REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chargeBee/latest
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.chargebee.com
- **Vendor API docs:** https://apidocs.chargebee.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Events](actions/list-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Bank Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Virtual Bank Accounts](actions/list-virtual-bank-accounts.md) | GET | Retrieves virtual bank accounts from ChargeBee. |

### Business Units

| Action | Method | Description |
| --- | --- | --- |
| [List Business Entities](actions/list-business-entities.md) | GET | Retrieves business entities from ChargeBee. |
| [Retrieve Business Entity](actions/retrieve-business-entity.md) | GET | Retrieves a business entity from ChargeBee. |

### Charges

| Action | Method | Description |
| --- | --- | --- |
| [List Unbilled Charges](actions/list-unbilled-charges.md) | GET | Retrieves unbilled charges from ChargeBee. |

### Coupons

| Action | Method | Description |
| --- | --- | --- |
| [List Coupons](actions/list-coupons.md) | GET | Retrieves coupons from ChargeBee. |
| [Retrieve Coupon](actions/retrieve-coupon.md) | GET | Retrieves a coupon from ChargeBee. |

### Credit Notes

| Action | Method | Description |
| --- | --- | --- |
| [List Credit Notes](actions/list-credit-notes.md) | GET | Retrieves credit notes from ChargeBee. |
| [List Promotional Credits](actions/list-promotional-credits.md) | GET | Retrieves promotional credits from ChargeBee. |
| [Retrieve Credit Note](actions/retrieve-credit-note.md) | GET | Retrieves a credit note from ChargeBee. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in ChargeBee. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from ChargeBee. |
| [Retrieve Customer](actions/retrieve-customer.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in ChargeBee. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET |  |
| [Retrieve Event](actions/retrieve-event.md) | GET | Retrieves an event from ChargeBee. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from ChargeBee. |
| [Retrieve Invoice](actions/retrieve-invoice.md) | GET | Retrieves an invoice from ChargeBee. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [List Items](actions/list-items.md) | GET | Retrieves items from ChargeBee. |
| [Retrieve Item](actions/retrieve-item.md) | GET | Retrieves an item from ChargeBee. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [List Usages](actions/list-usages.md) | GET | Retrieves usages from ChargeBee. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from ChargeBee. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [List Hosted Pages](actions/list-hosted-pages.md) | GET | Retrieves hosted pages from ChargeBee. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Sources](actions/list-payment-sources.md) | GET | Retrieves payment sources from ChargeBee. |
| [Retrieve Payment Source](actions/retrieve-payment-source.md) | GET | Retrieves a payment source from ChargeBee. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [List Item Prices](actions/list-item-prices.md) | GET | Retrieves item prices from ChargeBee. |
| [Retrieve Item Price](actions/retrieve-item-price.md) | GET | Retrieves an item price from ChargeBee. |

### Quotes

| Action | Method | Description |
| --- | --- | --- |
| [List Quotes](actions/list-quotes.md) | GET | Retrieves quotes from ChargeBee. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from ChargeBee. |
| [Retrieve Subscription](actions/retrieve-subscription.md) | GET |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from ChargeBee. |
| [Retrieve Transaction](actions/retrieve-transaction.md) | GET | Retrieves a transaction from ChargeBee. |

