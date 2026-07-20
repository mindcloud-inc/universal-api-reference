# STEL Order: Native API Reference

A consolidated summary of STEL Order's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://help.stelorder.com/hc/es/articles/7099722989213-API
- **OpenAPI specification:** https://app.stelorder.com/app/indexapi.html
- **API base URL:** `https://app.stelorder.com/app`

## Authentication

### API Key

Use the provider-native API key from the STAGE1_BUILD_INPUTS block. The provider expects it in the APIKEY header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
APIKEY: <apiKey>
```

[Official authentication documentation](https://help.stelorder.com/hc/es/articles/7099722989213-API)

## Pagination

Use `limit` in the query string to set the page size. Use `start` in the query string as the record offset; numbering starts at 0.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Account Categories](actions/list-account-categories.md) | `GET /accountCategories` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Addresses](actions/list-addresses.md) | `GET /addresses` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Bank Accounts](actions/list-bank-accounts.md) | `GET /bankAccounts` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Calendars](actions/list-calendars.md) | `GET /calendars` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Delivery Options](actions/list-delivery-options.md) | `GET /deliveryOptions` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Document States](actions/list-document-states.md) | `GET /documentStates` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Error Codes](actions/list-error-codes.md) | `GET /errorCodes` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Event Types](actions/list-event-types.md) | `GET /eventTypes` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Expense Categories](actions/list-expense-categories.md) | `GET /expenseCategories` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Expense States](actions/list-expense-states.md) | `GET /expenseStates` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Expenses](actions/list-expenses.md) | `GET /expenses` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Item Images](actions/list-item-images.md) | `GET /itemImages` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Item Rates](actions/list-item-rates.md) | `GET /itemRates` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Ordinary Invoice Receipts](actions/list-ordinary-invoice-receipts.md) | `GET /ordinaryInvoiceReceipts` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Ordinary Invoices](actions/list-ordinary-invoices.md) | `GET /ordinaryInvoices` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Payment Options](actions/list-payment-options.md) | `GET /paymentOptions` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Payment Terms](actions/list-payment-terms.md) | `GET /paymentTerms` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Potential Clients](actions/list-potential-clients.md) | `GET /potentialClients` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Product Categories](actions/list-product-categories.md) | `GET /productCategories` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Product Components](actions/list-product-components.md) | `GET /productComponents` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Product Warehouses](actions/list-product-warehouses.md) | `GET /productWarehouses` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Refund Invoice Receipts](actions/list-refund-invoice-receipts.md) | `GET /refundInvoiceReceipts` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Refund Invoices](actions/list-refund-invoices.md) | `GET /refundInvoices` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /salesOrders` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Services](actions/list-services.md) | `GET /services` | [docs](https://app.stelorder.com/app/indexapi.html) |
| [List Work Orders](actions/list-work-orders.md) | `GET /workOrders` | [docs](https://app.stelorder.com/app/indexapi.html) |
