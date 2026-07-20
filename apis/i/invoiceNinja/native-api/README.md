# Invoice Ninja: Native API Reference

A consolidated summary of Invoice Ninja's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.invoicing.co/
- **API base URL:** `https://invoicing.co/api/v1`

## Authentication

### API Key

Authenticate using X-API-TOKEN and the required X-Requested-With header.

### Credentials

- **API Key:** `apiKey` · required
- **Base URL:** `baseUrl` · required · Enter the full Invoice Ninja API root, including /api/v1.

Send these headers with each API request:

```http
X-API-TOKEN: <apiKey>
```

[Official authentication documentation](https://api-docs.invoicing.co/#section/Authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `meta.pagination.totalPages`. The current page number is read from `meta.pagination.currentPage`.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `sort_dir`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Client Actions](actions/bulk-client-actions.md) | `POST /clients/bulk` | [docs](https://api-docs.invoicing.co/#tag/clients/operation/bulkClients) |
| [Bulk Invoice Actions](actions/bulk-invoice-actions.md) | `POST /invoices/bulk` | [docs](https://api-docs.invoicing.co/#tag/invoices/operation/bulkInvoices) |
| [Bulk Quote Actions](actions/bulk-quote-actions.md) | `POST /quotes/bulk` | [docs](https://api-docs.invoicing.co/#tag/quotes/operation/bulkQuotes) |
| [Client Statement PDF](actions/client-statement-pdf.md) | `POST /client_statement` | [docs](https://api-docs.invoicing.co/#tag/clients/operation/clientStatement) |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://api-docs.invoicing.co/#tag/clients/operation/storeClient) |
| [Create Expense](actions/create-expense.md) | `POST /expenses` | [docs](https://api-docs.invoicing.co/#tag/expenses/operation/storeExpense) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://api-docs.invoicing.co/#tag/invoices/operation/storeInvoice) |
| [Create Payment](actions/create-payment.md) | `POST /payments` | [docs](https://api-docs.invoicing.co/#tag/payments/operation/storePayment) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://api-docs.invoicing.co/#tag/products/operation/storeProduct) |
| [Create Quote](actions/create-quote.md) | `POST /quotes` | [docs](https://api-docs.invoicing.co/#tag/quotes/operation/storeQuote) |
| [Create Recurring Invoice](actions/create-recurring-invoice.md) | `POST /recurring_invoices` | [docs](https://api-docs.invoicing.co/#tag/Recurring-Invoices/operation/storeRecurringInvoice) |
| [Create Vendor](actions/create-vendor.md) | `POST /vendors` | [docs](https://api-docs.invoicing.co/#tag/vendors/operation/storeVendor) |
| [Custom Invoice Action](actions/custom-invoice-action.md) | `GET /invoices/:id/:action` | [docs](https://api-docs.invoicing.co/#tag/invoices/operation/actionInvoice) |
| [Custom Quote Action](actions/custom-quote-action.md) | `GET /quotes/:id/:action` | [docs](https://api-docs.invoicing.co/#tag/quotes/operation/actionQuote) |
| [Download Invoice PDF](actions/download-invoice-pdf.md) | `GET /invoice/:invitation_key/download` | [docs](https://api-docs.invoicing.co/#tag/invoices/operation/downloadInvoiceByInvitation) |
| [Download Quote PDF](actions/download-quote-pdf.md) | `GET /quote/:invitation_key/download` | [docs](https://api-docs.invoicing.co/#tag/quotes/operation/downloadQuote) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://api-docs.invoicing.co/#tag/clients/operation/getClients) |
| [List Expenses](actions/list-expenses.md) | `GET /expenses` | [docs](https://api-docs.invoicing.co/#tag/expenses/operation/getExpenses) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://api-docs.invoicing.co/#tag/invoices/operation/getInvoices) |
| [List Payment Terms](actions/list-payment-terms.md) | `GET /payment_terms` | [docs](https://api-docs.invoicing.co/#tag/payment_terms/operation/getPaymentTerms) |
| [List Payments](actions/list-payments.md) | `GET /payments` | [docs](https://api-docs.invoicing.co/#tag/payments/operation/getPayments) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://api-docs.invoicing.co/#tag/products/operation/getProducts) |
| [List Quotes](actions/list-quotes.md) | `GET /quotes` | [docs](https://api-docs.invoicing.co/#tag/quotes/operation/getQuotes) |
| [List Recurring Invoices](actions/list-recurring-invoices.md) | `GET /recurring_invoices` | [docs](https://api-docs.invoicing.co/#tag/Recurring-Invoices/operation/getRecurringInvoices) |
| [List Tax Rates](actions/list-tax-rates.md) | `GET /tax_rates` | [docs](https://api-docs.invoicing.co/#tag/tax_rates/operation/getTaxRates) |
| [List Vendors](actions/list-vendors.md) | `GET /vendors` | [docs](https://api-docs.invoicing.co/#tag/vendors/operation/getVendors) |
| [Refund Payment](actions/refund-payment.md) | `POST /payments/refund` | [docs](https://api-docs.invoicing.co/#tag/payments/operation/storeRefund) |
| [Show Client](actions/show-client.md) | `GET /clients/:id` | [docs](https://api-docs.invoicing.co/#tag/clients/operation/showClient) |
| [Show Invoice](actions/show-invoice.md) | `GET /invoices/:id` | [docs](https://api-docs.invoicing.co/#tag/invoices/operation/showInvoice) |
| [Show Payment](actions/show-payment.md) | `GET /payments/:id` | [docs](https://api-docs.invoicing.co/#tag/payments/operation/showPayment) |
| [Show Product](actions/show-product.md) | `GET /products/:id` | [docs](https://api-docs.invoicing.co/#tag/products/operation/showProduct) |
| [Show Quote](actions/show-quote.md) | `GET /quotes/:id` | [docs](https://api-docs.invoicing.co/#tag/quotes/operation/showQuote) |
| [Show Recurring Invoice](actions/show-recurring-invoice.md) | `GET /recurring_invoices/:id` | [docs](https://api-docs.invoicing.co/#tag/Recurring-Invoices/operation/showRecurringInvoice) |
| [Update Client](actions/update-client.md) | `PUT /clients/:id` | [docs](https://api-docs.invoicing.co/#tag/clients/operation/updateClient) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:id` | [docs](https://api-docs.invoicing.co/#tag/invoices/operation/updateInvoice) |
| [Update Payment](actions/update-payment.md) | `PUT /payments/:id` | [docs](https://api-docs.invoicing.co/#tag/payments/operation/updatePayment) |
| [Update Product](actions/update-product.md) | `PUT /products/:id` | [docs](https://api-docs.invoicing.co/#tag/products/operation/updateProduct) |
| [Update Quote](actions/update-quote.md) | `PUT /quotes/:id` | [docs](https://api-docs.invoicing.co/#tag/quotes/operation/updateQuote) |
| [Update Recurring Invoice](actions/update-recurring-invoice.md) | `PUT /recurring_invoices/:id` | [docs](https://api-docs.invoicing.co/#tag/Recurring-Invoices/operation/updateRecurringInvoice) |
| [Update Tax Data](actions/update-tax-data.md) | `POST /clients/:client/updateTaxData` | [docs](https://api-docs.invoicing.co/#tag/clients/operation/updateClientTaxData) |
