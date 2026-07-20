# <img src="https://images.mindcloud.co/apps/icons/images-9_1774468626125.jpeg" alt="QuickFile logo" width="28" height="28"> QuickFile: Universal API

QuickFile is a cloud accounting platform for invoicing, banking, purchases, suppliers, reporting, and related bookkeeping workflows via the QuickFile API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quickFile/latest
- **Category:** Commerce / Accounting
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.quickfile.co.uk/
- **Vendor API docs:** https://api.quickfile.co.uk/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Chart Of Accounts](actions/get-chart-of-accounts.md) | GET |  |
| [List Bank Account Balances](actions/list-bank-account-balances.md) | GET |  |
| [List Bank Accounts](actions/list-bank-accounts.md) | GET |  |

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST |  |
| [Search Events](actions/search-events.md) | GET |  |

### Balance Sheets

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance Sheet](actions/get-balance-sheet.md) | GET |  |

### Company Infos

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST |  |
| [Get Client](actions/get-client.md) | GET |  |
| [Search Clients](actions/search-clients.md) | GET |  |
| [Update Client](actions/update-client.md) | PUT |  |

### Expenses

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase](actions/get-purchase.md) | GET |  |
| [Search Purchases](actions/search-purchases.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice PDF](actions/get-invoice-pdf.md) | GET |  |

### Income Statements

| Action | Method | Description |
| --- | --- | --- |
| [Get Profit And Loss](actions/get-profit-and-loss.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [Search Invoices](actions/search-invoices.md) | GET |  |

### Journal Entries

| Action | Method | Description |
| --- | --- | --- |
| [Get Journal](actions/get-journal.md) | GET |  |
| [Search Journals](actions/search-journals.md) | GET |  |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Methods](actions/list-payment-methods.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment](actions/create-payment.md) | POST |  |
| [Get Payment](actions/get-payment.md) | GET |  |
| [Search Payments](actions/search-payments.md) | GET |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Search Bank Transactions](actions/search-bank-transactions.md) | GET |  |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier](actions/create-supplier.md) | POST |  |
| [Get Supplier](actions/get-supplier.md) | GET |  |
| [Search Suppliers](actions/search-suppliers.md) | GET |  |
| [Update Supplier](actions/update-supplier.md) | PUT |  |

