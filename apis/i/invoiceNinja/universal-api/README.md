# <img src="https://images.mindcloud.co/apps/icons/invoice-ninja_1774026955720.png" alt="Invoice Ninja logo" width="28" height="28"> Invoice Ninja: Universal API

Create invoices, manage clients, track expenses, and get paid

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/invoiceNinja/latest
- **Category:** Commerce / Accounting
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.invoiceninja.com
- **Vendor API docs:** https://api-docs.invoicing.co/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Payment Terms](actions/list-payment-terms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-payment-terms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Client Actions](actions/bulk-client-actions.md) | PUT |  |
| [Client Statement PDF](actions/client-statement-pdf.md) | GET |  |
| [Create Client](actions/create-client.md) | POST |  |
| [List Clients](actions/list-clients.md) | GET |  |
| [Show Client](actions/show-client.md) | GET |  |
| [Update Client](actions/update-client.md) | PUT |  |
| [Update Tax Data](actions/update-tax-data.md) | PUT |  |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | POST |  |
| [List Expenses](actions/list-expenses.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Invoice Actions](actions/bulk-invoice-actions.md) | PUT |  |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [Custom Invoice Action](actions/custom-invoice-action.md) | PUT |  |
| [Download Invoice PDF](actions/download-invoice-pdf.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |
| [Show Invoice](actions/show-invoice.md) | GET |  |
| [Update Invoice](actions/update-invoice.md) | PUT |  |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment](actions/create-payment.md) | POST |  |
| [List Payments](actions/list-payments.md) | GET |  |
| [Refund Payment](actions/refund-payment.md) | PUT |  |
| [Show Payment](actions/show-payment.md) | GET |  |
| [Update Payment](actions/update-payment.md) | PUT |  |

### Payment Term

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Terms](actions/list-payment-terms.md) | GET |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [List Products](actions/list-products.md) | GET |  |
| [Show Product](actions/show-product.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Quote Actions](actions/bulk-quote-actions.md) | PUT |  |
| [Create Quote](actions/create-quote.md) | POST |  |
| [Custom Quote Action](actions/custom-quote-action.md) | PUT |  |
| [Download Quote PDF](actions/download-quote-pdf.md) | GET |  |
| [List Quotes](actions/list-quotes.md) | GET |  |
| [Show Quote](actions/show-quote.md) | GET |  |
| [Update Quote](actions/update-quote.md) | PUT |  |

### Recurring Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Recurring Invoice](actions/create-recurring-invoice.md) | POST |  |
| [List Recurring Invoices](actions/list-recurring-invoices.md) | GET |  |
| [Show Recurring Invoice](actions/show-recurring-invoice.md) | GET |  |
| [Update Recurring Invoice](actions/update-recurring-invoice.md) | PUT |  |

### Tax Rate

| Action | Method | Description |
| --- | --- | --- |
| [List Tax Rates](actions/list-tax-rates.md) | GET |  |

### Vendor

| Action | Method | Description |
| --- | --- | --- |
| [Create Vendor](actions/create-vendor.md) | POST |  |
| [List Vendors](actions/list-vendors.md) | GET |  |

