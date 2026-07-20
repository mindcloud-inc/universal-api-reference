# <img src="https://images.mindcloud.co/apps/icons/quick-books-online_1776804726327.png" alt="QuickBooks Online logo" width="28" height="28"> QuickBooks Online: Universal API

Manage invoices, customers, vendors, bills, reports, and accounting data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quickBooksOnline/latest
- **Category:** Commerce / Accounting
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://quickbooks.intuit.com/online
- **Vendor API docs:** https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickBooksOnline/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST |  |
| [Get Account](actions/get-account.md) | GET |  |
| [List Accounts](actions/list-accounts.md) | GET |  |

### Bills

| Action | Method | Description |
| --- | --- | --- |
| [Create Bill](actions/create-bill.md) | POST |  |
| [Get Bill](actions/get-bill.md) | GET |  |
| [List Bills](actions/list-bills.md) | GET |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Get Customer](actions/get-customer.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |

### Income Statements

| Action | Method | Description |
| --- | --- | --- |
| [Get Profit and Loss](actions/get-profit-and-loss.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |
| [Send Invoice](actions/send-invoice.md) | PUT |  |
| [Update Invoice](actions/update-invoice.md) | PUT |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST |  |
| [Get Item](actions/get-item.md) | GET |  |
| [List Items](actions/list-items.md) | GET |  |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order](actions/create-purchase-order.md) | POST |  |
| [Get Purchase Order](actions/get-purchase-order.md) | GET |  |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET |  |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Query](actions/query.md) | GET |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Update Sales Receipt](actions/update-sales-receipt.md) | PUT |  |

### Sales Receipt

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Receipts](actions/list-sales-receipts.md) | GET |  |

### Transaction Detail By Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction Detail by Account](actions/get-transaction-detail-by-account.md) | GET |  |

### Transaction List

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction List](actions/get-transaction-list.md) | GET |  |

### Transaction List By Vendor

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction List by Vendor](actions/get-transaction-list-by-vendor.md) | GET |  |

### Transaction List With Splits

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction List with Splits](actions/get-transaction-list-with-splits.md) | GET |  |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Create Vendor](actions/create-vendor.md) | POST |  |
| [Get Vendor](actions/get-vendor.md) | GET |  |
| [List Vendors](actions/list-vendors.md) | GET |  |

