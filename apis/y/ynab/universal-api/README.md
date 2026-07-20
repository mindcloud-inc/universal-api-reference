# <img src="https://images.mindcloud.co/apps/icons/ynab_1776300905938.png" alt="YNAB logo" width="28" height="28"> YNAB: Universal API

Manage budgets, accounts, categories, and transactions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ynab/latest
- **Category:** Commerce / Accounting
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.ynab.com
- **Vendor API docs:** https://api.ynab.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Plans](actions/list-plans.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from a YNAB plan. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from a YNAB plan. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from a YNAB plan. |
| [Get Month Category](actions/get-month-category.md) | GET | Retrieves a category for a specific month in YNAB. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from a YNAB plan. |

### Money Movement

| Action | Method | Description |
| --- | --- | --- |
| [List Money Movements](actions/list-money-movements.md) | GET | Retrieves money movements from a YNAB plan. |
| [List Month Money Movements](actions/list-month-money-movements.md) | GET | Retrieves money movements for a month in YNAB. |

### Money Movement Group

| Action | Method | Description |
| --- | --- | --- |
| [List Money Movement Groups](actions/list-money-movement-groups.md) | GET | Retrieves money movement groups from a YNAB plan. |
| [List Month Money Movement Groups](actions/list-month-money-movement-groups.md) | GET | Retrieves money movement groups for a month in YNAB. |

### Month

| Action | Method | Description |
| --- | --- | --- |
| [Get Month](actions/get-month.md) | GET | Retrieves a month from a YNAB plan. |
| [List Months](actions/list-months.md) | GET | Retrieves months from a YNAB plan. |

### Payee

| Action | Method | Description |
| --- | --- | --- |
| [Get Payee](actions/get-payee.md) | GET | Retrieves a payee from a YNAB plan. |
| [List Payees](actions/list-payees.md) | GET | Retrieves payees from a YNAB plan. |

### Payee Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Payee Location](actions/get-payee-location.md) | GET | Retrieves a payee location from a YNAB plan. |
| [List Payee Locations](actions/list-payee-locations.md) | GET | Retrieves payee locations from a YNAB plan. |
| [List Payee Locations For Payee](actions/list-payee-locations-for-payee.md) | GET | Retrieves payee locations for a payee in YNAB. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan](actions/get-plan.md) | GET | Retrieves a full plan export from YNAB. |
| [List Plans](actions/list-plans.md) | GET | Retrieves plans from YNAB. |

### Plan Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan Settings](actions/get-plan-settings.md) | GET | Retrieves plan settings from YNAB. |

### Scheduled Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Scheduled Transaction](actions/get-scheduled-transaction.md) | GET | Retrieves a scheduled transaction from a YNAB plan. |
| [List Scheduled Transactions](actions/list-scheduled-transactions.md) | GET | Retrieves scheduled transactions from a YNAB plan. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from a YNAB plan. |
| [List Account Transactions](actions/list-account-transactions.md) | GET | Retrieves transactions for an account in YNAB. |
| [List Category Transactions](actions/list-category-transactions.md) | GET | Retrieves transactions for a category in YNAB. |
| [List Month Transactions](actions/list-month-transactions.md) | GET | Retrieves transactions for a month in YNAB. |
| [List Payee Transactions](actions/list-payee-transactions.md) | GET | Retrieves transactions for a payee in YNAB. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from a YNAB plan. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves the authenticated user from YNAB. |

