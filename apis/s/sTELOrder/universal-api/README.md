# <img src="https://images.mindcloud.co/apps/icons/s-telorder_1776111394909.png" alt="STEL Order logo" width="28" height="28"> STEL Order: Universal API

STEL Order connector

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sTELOrder/latest
- **Category:** Commerce / ERP
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.stelorder.com/en/
- **Vendor API docs:** https://help.stelorder.com/hc/es/articles/7099722989213-API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Clients](actions/list-clients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [List Addresses](actions/list-addresses.md) | GET | Retrieves a list of addresses from STEL Order. |

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [List Item Images](actions/list-item-images.md) | GET | Retrieves a list of item images from STEL Order. |

### Bank Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Bank Accounts](actions/list-bank-accounts.md) | GET | Retrieves a list of bank accounts from STEL Order. |

### Calendars

| Action | Method | Description |
| --- | --- | --- |
| [List Calendars](actions/list-calendars.md) | GET | Retrieves a list of calendars from STEL Order. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Account Categories](actions/list-account-categories.md) | GET | Retrieves a list of account categories from STEL Order. |
| [List Event Types](actions/list-event-types.md) | GET | Retrieves a list of event types from STEL Order. |
| [List Expense Categories](actions/list-expense-categories.md) | GET | Retrieves a list of expense categories from STEL Order. |
| [List Product Categories](actions/list-product-categories.md) | GET | Retrieves a list of product categories from STEL Order. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from STEL Order. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Clients](actions/list-clients.md) | GET | Retrieves a list of clients from STEL Order. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves a list of events from STEL Order. |

### Expenses

| Action | Method | Description |
| --- | --- | --- |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves a list of expenses from STEL Order. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Ordinary Invoices](actions/list-ordinary-invoices.md) | GET | Retrieves a list of ordinary invoices from STEL Order. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [List Potential Clients](actions/list-potential-clients.md) | GET | Retrieves a list of potential clients from STEL Order. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Options](actions/list-payment-options.md) | GET | Retrieves a list of payment options from STEL Order. |

### Payment Terms

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Terms](actions/list-payment-terms.md) | GET | Retrieves a list of payment terms from STEL Order. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [List Ordinary Invoice Receipts](actions/list-ordinary-invoice-receipts.md) | GET | Retrieves a list of ordinary invoice receipts from STEL Order. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [List Item Rates](actions/list-item-rates.md) | GET | Retrieves a list of item rates from STEL Order. |

### Problems

| Action | Method | Description |
| --- | --- | --- |
| [List Error Codes](actions/list-error-codes.md) | GET | Retrieves a list of STEL Order API error codes. |

### Product Variants

| Action | Method | Description |
| --- | --- | --- |
| [List Product Components](actions/list-product-components.md) | GET | Retrieves a list of product components from STEL Order. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from STEL Order. |

### Refunds

| Action | Method | Description |
| --- | --- | --- |
| [List Refund Invoice Receipts](actions/list-refund-invoice-receipts.md) | GET | Retrieves a list of refund invoice receipts from STEL Order. |
| [List Refund Invoices](actions/list-refund-invoices.md) | GET | Retrieves a list of refund invoices from STEL Order. |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Retrieves a list of sales orders from STEL Order. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List Services](actions/list-services.md) | GET | Retrieves a list of services from STEL Order. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [List Delivery Options](actions/list-delivery-options.md) | GET | Retrieves a list of delivery options from STEL Order. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Document States](actions/list-document-states.md) | GET | Retrieves a list of document states from STEL Order. |
| [List Expense States](actions/list-expense-states.md) | GET | Retrieves a list of expense states from STEL Order. |

### Warehouses

| Action | Method | Description |
| --- | --- | --- |
| [List Product Warehouses](actions/list-product-warehouses.md) | GET | Retrieves a list of product warehouses from STEL Order. |

### Work Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Work Orders](actions/list-work-orders.md) | GET | Retrieves a list of work orders from STEL Order. |

