# <img src="https://images.mindcloud.co/apps/icons/6656011d855a8cb0b8f6e6ae-chargeback-favicon_1776821231995.png" alt="Chargback logo" width="28" height="28"> Chargback: Universal API

Chargeback helps merchants monitor chargeback alerts, invoices, business accounts, and webhook subscriptions through its public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chargback/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.chargeback.io
- **Vendor API docs:** https://api.chargeback.io/api/public/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Business Accounts](actions/list-business-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargback/latest/actions/list-business-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Change Alert Status](actions/change-alert-status.md) | PUT | Updates an existing alert status in Chargback. |
| [Get Alert](actions/get-alert.md) | GET | Retrieves detailed alert records from Chargback. |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves chargeback alert records from Chargback. |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST | Creates a new API key in Chargback. |
| [Delete API Key](actions/delete-api-key.md) | DELETE | Deletes an existing API key from Chargback. |
| [List API Keys](actions/list-api-keys.md) | GET | Retrieves API key records from Chargback. |
| [Regenerate API Key](actions/regenerate-api-key.md) | PUT | Regenerates an existing API key in Chargback. |

### Business Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Business Account](actions/get-business-account.md) | GET |  |
| [List Business Accounts](actions/list-business-accounts.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves billing invoice records from Chargback. |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a new webhook subscription in Chargback. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes an existing webhook subscription from Chargback. |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | GET | Retrieves webhook subscription details from Chargback. |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves webhook subscription records from Chargback. |

