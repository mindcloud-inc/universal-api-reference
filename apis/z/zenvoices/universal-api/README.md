# <img src="https://images.mindcloud.co/apps/icons/favicon-www-zenvoices-com-48x48_1777046164428.png" alt="Zenvoices logo" width="28" height="28"> Zenvoices: Universal API

Zenvoices is an accounts payable and financial operations platform with a public API for administrations, accounts, transactions, inbox documents, master data, and webhook subscriptions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zenvoices/latest
- **Category:** Commerce / Accounting
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zenvoices.com/
- **Vendor API docs:** https://www.zenvoices.com/blog/public-api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Token Login](actions/token-login.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenvoices/latest/actions/token-login?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Token Login](actions/token-login.md) | GET | Retrieves an access token from Zenvoices. |

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account By Code](actions/get-account-by-code.md) | GET | Retrieves an account from Zenvoices by code. |
| [Get Account By External ID](actions/get-account-by-external-id.md) | GET | Retrieves an account from Zenvoices by external ID. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from your Zenvoices workspace. |

### Administration

| Action | Method | Description |
| --- | --- | --- |
| [Get Administration](actions/get-administration.md) | GET | Retrieves an administration from your Zenvoices workspace. |
| [List Administrations](actions/list-administrations.md) | GET | Retrieves administrations from your Zenvoices workspace. |

### Cost Centre

| Action | Method | Description |
| --- | --- | --- |
| [List Cost Centres](actions/list-cost-centres.md) | GET | Retrieves cost centres from your Zenvoices workspace. |

### Cost Unit

| Action | Method | Description |
| --- | --- | --- |
| [List Cost Units](actions/list-cost-units.md) | GET | Retrieves cost units from your Zenvoices workspace. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee By Code](actions/get-employee-by-code.md) | GET | Retrieves an employee from Zenvoices by code. |
| [List Employees](actions/list-employees.md) | GET | Retrieves employees from your Zenvoices workspace. |

### Financial Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Financial Transaction](actions/get-financial-transaction.md) | GET | Retrieves a financial transaction from your Zenvoices workspace. |
| [List Financial Transactions](actions/list-financial-transactions.md) | GET | Retrieves financial transactions from your Zenvoices workspace. |

### Inbox Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Inbox Document](actions/get-inbox-document.md) | GET | Retrieves an inbox document from your Zenvoices workspace. |
| [List Inbox Documents](actions/list-inbox-documents.md) | GET | Retrieves inbox documents from your Zenvoices workspace. |

### Ledger Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Ledger Account By Code](actions/get-ledger-account-by-code.md) | GET | Retrieves a ledger account from Zenvoices by code. |
| [List Ledger Accounts](actions/list-ledger-accounts.md) | GET | Retrieves ledger accounts from your Zenvoices workspace. |

### Payment Condition

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Conditions](actions/list-payment-conditions.md) | GET | Retrieves payment conditions from your Zenvoices workspace. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product By Code](actions/get-product-by-code.md) | GET | Retrieves a product from Zenvoices by code. |
| [List Products](actions/list-products.md) | GET | Retrieves products from your Zenvoices workspace. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project By Code](actions/get-project-by-code.md) | GET | Retrieves a project from Zenvoices by code. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from your Zenvoices workspace. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase Order](actions/get-purchase-order.md) | GET | Retrieves a purchase order from Zenvoices by purchase order number. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase orders from your Zenvoices workspace. |

### Tax Code

| Action | Method | Description |
| --- | --- | --- |
| [List Tax Codes](actions/list-tax-codes.md) | GET | Retrieves tax codes from your Zenvoices workspace. |

### Webhook Event

| Action | Method | Description |
| --- | --- | --- |
| [List Available Webhooks](actions/list-available-webhooks.md) | GET | Retrieves available webhook event names from Zenvoices. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves webhook subscriptions from your Zenvoices workspace. |

