# <img src="https://images.mindcloud.co/apps/icons/invoice-berry_1774303470382.png" alt="InvoiceBerry logo" width="28" height="28"> InvoiceBerry: Universal API

Create invoices and quotes, track expenses, and manage clients

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/invoiceBerry/latest
- **Category:** Commerce / Accounting
- **Actions:** 45
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.invoiceberry.com
- **Vendor API docs:** https://www.invoiceberry.com/api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Currencies](actions/list-currencies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (45)

### Credit Notes

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Note](actions/get-credit-note.md) | GET |  |
| [Get Total Credit Notes](actions/get-total-credit-notes.md) | GET |  |
| [List Credit Notes](actions/list-credit-notes.md) | GET |  |
| [Update Credit Note](actions/update-credit-note.md) | PUT |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Client](actions/get-client.md) | GET |  |
| [Get Total Clients](actions/get-total-clients.md) | GET |  |
| [List Client Reports](actions/list-client-reports.md) | GET |  |
| [List Clients](actions/list-clients.md) | GET |  |
| [List Credit Note Client Contacts](actions/list-credit-note-client-contacts.md) | GET |  |
| [List Invoice Client Contacts](actions/list-invoice-client-contacts.md) | GET |  |
| [List Quote Client Contacts](actions/list-quote-client-contacts.md) | GET |  |
| [Update Client](actions/update-client.md) | PUT |  |

### Expenses

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | POST |  |
| [Get Expense](actions/get-expense.md) | GET |  |
| [Get Total Expenses](actions/get-total-expenses.md) | GET |  |
| [Update Expense](actions/update-expense.md) | PUT |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [Get Recurring Invoice](actions/get-recurring-invoice.md) | GET |  |
| [Get Total Invoices](actions/get-total-invoices.md) | GET |  |
| [Get Total Recurring Invoices](actions/get-total-recurring-invoices.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |
| [List Recurring Invoices](actions/list-recurring-invoices.md) | GET |  |
| [Update Invoice](actions/update-invoice.md) | PUT |  |
| [Update Recurring Invoice](actions/update-recurring-invoice.md) | PUT |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST |  |
| [Get Item](actions/get-item.md) | GET |  |
| [Get Total Items](actions/get-total-items.md) | GET |  |
| [List Items](actions/list-items.md) | GET |  |
| [Update Item](actions/update-item.md) | PUT |  |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Methods](actions/list-payment-methods.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Credit History](actions/get-client-credit-history.md) | GET |  |

### Tax Rates

| Action | Method | Description |
| --- | --- | --- |
| [Create Tax](actions/create-tax.md) | POST |  |
| [List Taxes](actions/list-taxes.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense Category](actions/create-expense-category.md) | POST |  |
| [Get Quote](actions/get-quote.md) | GET |  |
| [Get Total Quotes](actions/get-total-quotes.md) | GET |  |
| [List Countries](actions/list-countries.md) | GET |  |
| [List Currencies](actions/list-currencies.md) | GET |  |
| [List Expense Categories](actions/list-expense-categories.md) | GET |  |
| [List Languages](actions/list-languages.md) | GET |  |
| [List Quotes](actions/list-quotes.md) | GET |  |
| [List Recurring Frequencies](actions/list-recurring-frequencies.md) | GET |  |
| [Update Quote](actions/update-quote.md) | PUT |  |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense Vendor](actions/create-expense-vendor.md) | POST |  |
| [List Expense Vendors](actions/list-expense-vendors.md) | GET |  |

