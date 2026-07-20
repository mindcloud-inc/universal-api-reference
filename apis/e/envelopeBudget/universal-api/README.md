# <img src="https://images.mindcloud.co/apps/icons/envelope-budget_1774902359764.png" alt="EnvelopeBudget logo" width="28" height="28"> EnvelopeBudget: Universal API

Track budgets, manage envelopes, and sync transactions with EnvelopeBudget

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/envelopeBudget/latest
- **Category:** Commerce / Accounting
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://envelopebudget.com
- **Vendor API docs:** https://envelopebudget.com/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Budgets](actions/list-budgets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envelopeBudget/latest/actions/list-budgets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST |  |
| [Delete Account](actions/delete-account.md) | DELETE |  |
| [Get Account](actions/get-account.md) | GET |  |
| [List Accounts](actions/list-accounts.md) | GET |  |
| [Update Account](actions/update-account.md) | PUT |  |

### Budget

| Action | Method | Description |
| --- | --- | --- |
| [Get Budget](actions/get-budget.md) | GET |  |
| [List Budgets](actions/list-budgets.md) | GET |  |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST |  |
| [Delete Category](actions/delete-category.md) | DELETE |  |
| [Get Category](actions/get-category.md) | GET |  |
| [List Categories](actions/list-categories.md) | GET |  |
| [Update Category](actions/update-category.md) | PUT |  |

### Envelope

| Action | Method | Description |
| --- | --- | --- |
| [Delete Envelope](actions/delete-envelope.md) | DELETE |  |
| [Get Envelope](actions/get-envelope.md) | GET |  |
| [List Envelopes](actions/list-envelopes.md) | GET |  |
| [Update Envelope](actions/update-envelope.md) | PUT |  |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | POST |  |
| [Delete Transaction](actions/delete-transaction.md) | DELETE |  |
| [Get Transaction](actions/get-transaction.md) | GET |  |
| [List Transactions](actions/list-transactions.md) | GET |  |
| [Patch Transaction](actions/patch-transaction.md) | PUT |  |

