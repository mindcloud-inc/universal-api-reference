# <img src="https://images.mindcloud.co/apps/icons/6272d6e8457db09c4dd24f50-favicon-32x32_1776093363134.png" alt="Tarvent logo" width="28" height="28"> Tarvent: Universal API

Manage audiences, campaigns, journeys, and transactional email in Tarvent

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tarvent/latest
- **Category:** Communication / Email Communications
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tarvent.com
- **Vendor API docs:** https://developer.tarvent.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from Tarvent. |

### Account Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Get Account API Key](actions/get-account-api-key.md) | GET | Retrieves an account API key from Tarvent by ID. |
| [List Account API Keys](actions/list-account-api-keys.md) | GET | Retrieves account API keys from Tarvent. |

### Account Entity

| Action | Method | Description |
| --- | --- | --- |
| [Search Account Entities](actions/search-account-entities.md) | GET | Finds account entities in Tarvent by search text. |

### Account Export

| Action | Method | Description |
| --- | --- | --- |
| [List Exports](actions/list-exports.md) | GET | Retrieves exports from Tarvent. |

### Account Growth Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Monthly Growth Stats](actions/get-monthly-growth-stats.md) | GET | Retrieves monthly growth stats from Tarvent. |

### Account Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Invoice](actions/get-account-invoice.md) | GET | Retrieves an account invoice from Tarvent by ID. |
| [List Account Invoices](actions/list-account-invoices.md) | GET | Retrieves account invoices from Tarvent. |

### Account Plan Stat

| Action | Method | Description |
| --- | --- | --- |
| [List Account Plan Stats](actions/list-account-plan-stats.md) | GET | Retrieves account plan stats from Tarvent. |

### Audience

| Action | Method | Description |
| --- | --- | --- |
| [List Audiences](actions/list-audiences.md) | GET | Retrieves audiences from Tarvent. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Tarvent. |

### Custom Report

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Reports](actions/list-custom-reports.md) | GET | Retrieves custom reports from Tarvent. |

### Integration Partner

| Action | Method | Description |
| --- | --- | --- |
| [List Integration Partners](actions/list-integration-partners.md) | GET | Retrieves integration partners from Tarvent. |

### Journey

| Action | Method | Description |
| --- | --- | --- |
| [List Journeys](actions/list-journeys.md) | GET | Retrieves journeys from Tarvent. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Plans](actions/list-plans.md) | GET | Retrieves plans from Tarvent. |

### Suppression Filter

| Action | Method | Description |
| --- | --- | --- |
| [List Suppression Filters](actions/list-suppression-filters.md) | GET | Retrieves suppression filters from Tarvent. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Tarvent. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from Tarvent. |

### User Notification

| Action | Method | Description |
| --- | --- | --- |
| [List User Notifications](actions/list-user-notifications.md) | GET | Retrieves user notifications from Tarvent. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Tarvent. |

