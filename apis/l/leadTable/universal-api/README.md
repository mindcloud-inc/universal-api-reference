# <img src="https://images.mindcloud.co/apps/icons/lead-table_1776951067063.png" alt="LeadTable logo" width="28" height="28"> LeadTable: Universal API

LeadTable is a white-label lead management platform for agencies to manage customers, campaigns, leads, files, and webhook subscriptions through the official LeadTable External API v3.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leadTable/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lead-table.com
- **Vendor API docs:** https://docs.lead-table.com/guide/leadtable-docs/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check authentication](actions/check-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/check-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create campaign](actions/create-campaign.md) | POST |  |
| [List customer campaigns](actions/list-customer-campaigns.md) | GET |  |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Check authentication](actions/check-authentication.md) | GET |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create customer](actions/create-customer.md) | POST |  |
| [List customers](actions/list-customers.md) | GET |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Attach webhook](actions/attach-webhook.md) | POST |  |
| [Detach webhook](actions/detach-webhook.md) | DELETE |  |
| [Poll webhook event](actions/poll-webhook-event.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Upload lead file](actions/upload-lead-file.md) | POST |  |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Create lead](actions/create-lead.md) | POST |  |
| [Get lead](actions/get-lead.md) | GET |  |
| [List campaign leads](actions/list-campaign-leads.md) | GET |  |
| [Search leads by email](actions/search-leads-by-email.md) | GET |  |
| [Update lead description](actions/update-lead-description.md) | PUT |  |
| [Upsert lead field](actions/upsert-lead-field.md) | PUT |  |

