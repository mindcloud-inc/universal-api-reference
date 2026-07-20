# <img src="https://images.mindcloud.co/apps/icons/recurly_1773712042311.png" alt="Recurly logo" width="28" height="28"> Recurly: Universal API

Subscription billing and recurring revenue platform for managing accounts, subscriptions, invoices, transactions, plans, and pricing.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/recurly/latest
- **Category:** Commerce
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://recurly.com/
- **Vendor API docs:** https://recurly.com/developers/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST |  |
| [Deactivate Account](actions/deactivate-account.md) | DELETE |  |
| [Fetch Account](actions/fetch-account.md) | GET |  |
| [Fetch Account Balance](actions/fetch-account-balance.md) | GET |  |
| [List Accounts](actions/list-accounts.md) | GET |  |
| [Reactivate Account](actions/reactivate-account.md) | PUT |  |
| [Update Account](actions/update-account.md) | PUT |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Invoice](actions/fetch-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Plan](actions/fetch-plan.md) | GET |  |
| [List Plans](actions/list-plans.md) | GET |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [List Sites](actions/list-sites.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT |  |
| [Create Subscription](actions/create-subscription.md) | POST |  |
| [Fetch Preview Renewal](actions/fetch-preview-renewal.md) | GET |  |
| [Fetch Subscription](actions/fetch-subscription.md) | GET |  |
| [List Account Subscriptions](actions/list-account-subscriptions.md) | GET |  |
| [List Subscriptions](actions/list-subscriptions.md) | GET |  |
| [Pause Subscription](actions/pause-subscription.md) | PUT |  |
| [Reactivate Subscription](actions/reactivate-subscription.md) | PUT |  |
| [Update Subscription](actions/update-subscription.md) | PUT |  |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Transaction](actions/fetch-transaction.md) | GET |  |
| [List Transactions](actions/list-transactions.md) | GET |  |

