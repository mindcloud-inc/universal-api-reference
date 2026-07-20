# <img src="https://images.mindcloud.co/apps/icons/sales-drive_1776454392944.png" alt="SalesDrive logo" width="28" height="28"> SalesDrive: Universal API

SalesDrive is a Ukrainian CRM for online stores and sales teams, with API coverage for orders, products, payments, documents, calls, delivery/payment metadata, and currency rates.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/salesDrive/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://salesdrive.com.ua/
- **Vendor API docs:** https://salesdrive.com.ua/knowledge/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Order Statuses](actions/list-order-statuses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-order-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Act

| Action | Method | Description |
| --- | --- | --- |
| [List Acts](actions/list-acts.md) | GET | Retrieves a list of act documents from SalesDrive. |

### Cash Order

| Action | Method | Description |
| --- | --- | --- |
| [List Cash Orders](actions/list-cash-orders.md) | GET | Retrieves a list of cash orders from SalesDrive. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Upsert Categories](actions/upsert-categories.md) | PUT | Creates or updates categories in SalesDrive. |

### Check

| Action | Method | Description |
| --- | --- | --- |
| [List Checks](actions/list-checks.md) | GET | Retrieves a list of checks from SalesDrive. |

### Contract

| Action | Method | Description |
| --- | --- | --- |
| [List Contracts](actions/list-contracts.md) | GET | Retrieves a list of contracts from SalesDrive. |

### Currency Rate

| Action | Method | Description |
| --- | --- | --- |
| [List Currency Rates](actions/list-currency-rates.md) | GET | Retrieves current currency rates from SalesDrive. |
| [Update Currency Rates](actions/update-currency-rates.md) | PUT | Updates current currency rates in SalesDrive. |

### Delivery Method

| Action | Method | Description |
| --- | --- | --- |
| [List Delivery Methods](actions/list-delivery-methods.md) | GET | Retrieves available delivery methods from SalesDrive. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves a list of invoices from SalesDrive. |

### Manager

| Action | Method | Description |
| --- | --- | --- |
| [Get Manager By Phone Number](actions/get-manager-by-phone-number.md) | GET | Retrieves manager and contact details by phone number in SalesDrive. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in SalesDrive. |
| [List Orders](actions/list-orders.md) | GET | Retrieves a list of orders from SalesDrive. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in SalesDrive. |

### Order Note

| Action | Method | Description |
| --- | --- | --- |
| [Add Order Note](actions/add-order-note.md) | POST | Adds a note to an order in SalesDrive. |

### Order Status

| Action | Method | Description |
| --- | --- | --- |
| [List Order Statuses](actions/list-order-statuses.md) | GET | Retrieves available order statuses from SalesDrive. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET | Retrieves a list of payments from SalesDrive. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves available payment methods from SalesDrive. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Upsert Products](actions/upsert-products.md) | PUT | Creates or updates products in SalesDrive. |

### Product Arrival

| Action | Method | Description |
| --- | --- | --- |
| [List Product Arrivals](actions/list-product-arrivals.md) | GET | Retrieves product arrival records from SalesDrive. |

### Sales Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Invoices](actions/list-sales-invoices.md) | GET | Retrieves a list of sales invoices from SalesDrive. |

