# <img src="https://images.mindcloud.co/apps/icons/campfire_1773946662982.png" alt="Campfire logo" width="28" height="28"> Campfire: Universal API

Manage cash management, accounting, AP, AR, and settings data in Campfire

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/campfire/latest
- **Category:** Commerce / Accounting
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://meetcampfire.com
- **Vendor API docs:** https://docs.campfire.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Chart Entities](actions/list-chart-entities.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/list-chart-entities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [List Fixed Assets](actions/list-fixed-assets.md) | GET | Retrieves fixed assets from Campfire. |
| [Retrieve Fixed Asset](actions/retrieve-fixed-asset.md) | GET | Retrieves a fixed asset from Campfire. |

### Bank Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Bank Accounts](actions/list-bank-accounts.md) | GET | Retrieves bank accounts from Campfire. |
| [Retrieve Bank Account](actions/retrieve-bank-account.md) | GET | Retrieves a bank account from Campfire. |

### Bank Feed Transactions

| Action | Method | Description |
| --- | --- | --- |
| [List Bank Transactions](actions/list-bank-transactions.md) | GET | Retrieves bank transactions from Campfire. |
| [Retrieve Bank Transaction](actions/retrieve-bank-transaction.md) | GET | Retrieves a bank transaction from Campfire. |

### Bills

| Action | Method | Description |
| --- | --- | --- |
| [List Accounting Bills](actions/list-accounting-bills.md) | GET | Retrieves accounting bills from Campfire. |
| [Retrieve Accounting Bill](actions/retrieve-accounting-bill.md) | GET | Retrieves an accounting bill from Campfire. |

### Budgets

| Action | Method | Description |
| --- | --- | --- |
| [List Budgets](actions/list-budgets.md) | GET | Retrieves budgets from Campfire. |
| [Retrieve Budget](actions/retrieve-budget.md) | GET | Retrieves a budget from Campfire. |

### Credit Notes

| Action | Method | Description |
| --- | --- | --- |
| [List Credit Memos](actions/list-credit-memos.md) | GET | Retrieves credit memos from Campfire. |
| [Retrieve Credit Memo](actions/retrieve-credit-memo.md) | GET | Retrieves a credit memo from Campfire. |

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | GET | Retrieves departments from Campfire. |
| [Retrieve Department](actions/retrieve-department.md) | GET | Retrieves a department from Campfire. |

### General Ledger Transactions

| Action | Method | Description |
| --- | --- | --- |
| [List Chart Transactions](actions/list-chart-transactions.md) | GET | Retrieves chart transactions from Campfire. |
| [Retrieve Chart Transaction](actions/retrieve-chart-transaction.md) | GET | Retrieves a chart transaction from Campfire. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Campfire. |
| [Retrieve Invoice](actions/retrieve-invoice.md) | GET | Retrieves an invoice from Campfire. |

### Journal Entries

| Action | Method | Description |
| --- | --- | --- |
| [List Journal Entries](actions/list-journal-entries.md) | GET | Retrieves journal entries from Campfire. |
| [Retrieve Journal Entry](actions/retrieve-journal-entry.md) | GET | Retrieves a journal entry from Campfire. |

### Legal Entities

| Action | Method | Description |
| --- | --- | --- |
| [List Chart Entities](actions/list-chart-entities.md) | GET | Retrieves chart entities from Campfire. |
| [Retrieve Chart Entity](actions/retrieve-chart-entity.md) | GET | Retrieves a chart entity from Campfire. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [List Entity Access](actions/list-entity-access.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET |  |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [List Vendors](actions/list-vendors.md) | GET | Retrieves vendors from Campfire. |
| [Retrieve Vendor](actions/retrieve-vendor.md) | GET | Retrieves a vendor from Campfire. |

