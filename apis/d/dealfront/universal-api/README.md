# <img src="https://images.mindcloud.co/apps/icons/images-2_1773684456651.png" alt="Dealfront logo" width="28" height="28"> Dealfront: Universal API

Identify website visitors, accounts, custom feeds, leads, and visit activity from Dealfront's Leadfeeder API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dealfront/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dealfront.com/
- **Vendor API docs:** https://docs.leadfeeder.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Dealfront. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Dealfront. |

### Custom Feed

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Feed](actions/get-custom-feed.md) | GET | Retrieves a custom feed from Dealfront. |
| [List Custom Feeds](actions/list-custom-feeds.md) | GET | Retrieves custom feeds from Dealfront. |

### Feed Export

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Export Status](actions/get-feed-export-status.md) | GET | Retrieves feed export status from Dealfront. |
| [Request Feed Export](actions/request-feed-export.md) | POST | Creates a new feed export request in Dealfront. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from Dealfront. |
| [List Custom Feed Leads](actions/list-custom-feed-leads.md) | GET | Retrieves leads for a custom feed in Dealfront. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from Dealfront. |

### Timeline Row

| Action | Method | Description |
| --- | --- | --- |
| [Download Feed Report](actions/download-feed-report.md) | GET | Retrieves a feed report from Dealfront. |

### Tracking Script

| Action | Method | Description |
| --- | --- | --- |
| [Get Website Tracking Script](actions/get-website-tracking-script.md) | GET | Retrieves a website tracking script from Dealfront. |

### Visit

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Visits](actions/list-lead-visits.md) | GET | Retrieves visits for a lead in Dealfront. |
| [List Visits](actions/list-visits.md) | GET | Retrieves visits from Dealfront. |

