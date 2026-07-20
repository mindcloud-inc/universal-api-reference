# <img src="https://images.mindcloud.co/apps/icons/favicon-20_1775595119704.png" alt="PocketSmith logo" width="28" height="28"> PocketSmith: Universal API

Track budgets, accounts, transactions, and cashflow forecasts with PocketSmith personal finance software.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pocketSmith/latest
- **Category:** Commerce / Accounting
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pocketsmith.com/
- **Vendor API docs:** https://developers.pocketsmith.com/docs/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authorised User](actions/get-authorised-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/get-authorised-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts In User](actions/list-accounts-in-user.md) | GET | Retrieves accounts for a PocketSmith user. |

### Budget

| Action | Method | Description |
| --- | --- | --- |
| [List Budget For User](actions/list-budget-for-user.md) | GET | Retrieves budget entries for a PocketSmith user. |

### Budget Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Budget Summary For User](actions/get-budget-summary-for-user.md) | GET | Retrieves a budget summary for a PocketSmith user. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category In User](actions/create-category-in-user.md) | POST | Creates a category for a PocketSmith user. |
| [Delete Category](actions/delete-category.md) | DELETE | Deletes a PocketSmith category. |
| [Get Category](actions/get-category.md) | GET | Retrieves a PocketSmith category. |
| [List Categories In User](actions/list-categories-in-user.md) | GET | Retrieves categories for a PocketSmith user. |
| [Update Category](actions/update-category.md) | PUT | Updates a PocketSmith category. |

### Category Rule

| Action | Method | Description |
| --- | --- | --- |
| [Create Category Rule In Category](actions/create-category-rule-in-category.md) | POST | Creates a category rule for a PocketSmith category. |
| [List Category Rules In User](actions/list-category-rules-in-user.md) | GET | Retrieves category rules for a PocketSmith user. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [Get Currency](actions/get-currency.md) | GET | Retrieves a PocketSmith currency. |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves PocketSmith currencies. |

### Forecast Cache

| Action | Method | Description |
| --- | --- | --- |
| [Delete Forecast Cache For User](actions/delete-forecast-cache-for-user.md) | DELETE | Deletes the forecast cache for a PocketSmith user. |

### Institution

| Action | Method | Description |
| --- | --- | --- |
| [Create Institution In User](actions/create-institution-in-user.md) | POST | Creates an institution for a PocketSmith user. |
| [Delete Institution](actions/delete-institution.md) | DELETE | Deletes a PocketSmith institution. |
| [Get Institution](actions/get-institution.md) | GET | Retrieves a PocketSmith institution. |
| [List Institutions In User](actions/list-institutions-in-user.md) | GET | Retrieves institutions for a PocketSmith user. |
| [Update Institution](actions/update-institution.md) | PUT | Updates a PocketSmith institution. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions In Categories](actions/list-transactions-in-categories.md) | GET | Retrieves transactions for PocketSmith categories. |
| [List Transactions In User](actions/list-transactions-in-user.md) | GET | Retrieves transactions for a PocketSmith user. |

### Transaction Account

| Action | Method | Description |
| --- | --- | --- |
| [List Transaction Accounts In User](actions/list-transaction-accounts-in-user.md) | GET | Retrieves transaction accounts for a PocketSmith user. |

### Trend Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Get Trend Analysis For User](actions/get-trend-analysis-for-user.md) | GET | Retrieves trend analysis for a PocketSmith user. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authorised User](actions/get-authorised-user.md) | GET | Retrieves the authorised PocketSmith user. |
| [Get User](actions/get-user.md) | GET | Retrieves a PocketSmith user. |

