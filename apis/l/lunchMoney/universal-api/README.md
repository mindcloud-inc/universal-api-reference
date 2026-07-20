# <img src="https://images.mindcloud.co/apps/icons/lunch-money_1775833535813.png" alt="Lunch Money logo" width="28" height="28"> Lunch Money: Universal API

Lunch Money is a personal finance and budgeting platform. This app wraps the official Lunch Money v2 API for budgets, categories, accounts, transactions, tags, recurring items, and account summary data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lunchMoney/latest
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lunchmoney.app
- **Vendor API docs:** https://alpha.lunchmoney.dev/v2/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get current user](actions/get-me.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Delete a file attachment](actions/delete-transaction-attachment.md) | DELETE |  |
| [Get transaction attachment download URL](actions/get-transaction-attachment-url.md) | GET |  |

### Bank Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Create a manual account](actions/create-manual-account.md) | POST |  |
| [Delete a manual account](actions/delete-manual-account.md) | DELETE |  |
| [Get all manual accounts](actions/get-all-manual-accounts.md) | GET |  |
| [Get all accounts synced via Plaid](actions/get-all-plaid-accounts.md) | GET |  |
| [Get a single manual account](actions/get-manual-account-by-id.md) | GET |  |
| [Update an existing manual account](actions/update-manual-account.md) | PUT |  |

### Budgets

| Action | Method | Description |
| --- | --- | --- |
| [Delete budget](actions/delete-budget.md) | DELETE |  |
| [Get budget settings](actions/get-budget-settings.md) | GET |  |
| [Upsert budget](actions/upsert-budget.md) | PUT |  |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create a new category or category group](actions/create-category.md) | POST |  |
| [Delete a category or category group](actions/delete-category.md) | DELETE |  |
| [Get all categories](actions/get-all-categories.md) | GET |  |
| [Get a single category](actions/get-category-by-id.md) | GET |  |
| [Update an existing category or category group](actions/update-category.md) | PUT |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get budget summary](actions/get-budget-summary.md) | GET |  |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get all recurring items](actions/get-all-recurring.md) | GET |  |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create a new tag](actions/create-tag.md) | POST |  |
| [Delete a tag](actions/delete-tag.md) | DELETE |  |
| [Get all tags](actions/get-all-tags.md) | GET |  |
| [Get a single tag](actions/get-tag-by-id.md) | GET |  |
| [Update an existing tag](actions/update-tag.md) | PUT |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Attach a file to a transaction](actions/attach-file-to-transaction.md) | POST |  |
| [Create transactions](actions/create-new-transactions.md) | POST |  |
| [Delete a transaction](actions/delete-transaction-by-id.md) | DELETE |  |
| [Bulk delete existing transactions](actions/delete-transactions.md) | DELETE |  |
| [Get all transactions](actions/get-all-transactions.md) | GET |  |
| [Get a single transaction](actions/get-transaction-by-id.md) | GET |  |
| [Create a transaction group](actions/group-transactions.md) | POST |  |
| [Split a transaction](actions/split-transaction.md) | PUT |  |
| [Delete a transaction group](actions/ungroup-transactions.md) | DELETE |  |
| [Unsplit a transaction](actions/unsplit-transaction.md) | DELETE |  |
| [Update an existing transaction](actions/update-transaction.md) | PUT |  |
| [Update multiple transactions](actions/update-transactions.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get current user](actions/get-me.md) | GET |  |

