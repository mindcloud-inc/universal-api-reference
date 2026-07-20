# <img src="https://images.mindcloud.co/apps/icons/leadfeeder-logo_1776095903195.jpeg" alt="Leadfeeder logo" width="28" height="28"> Leadfeeder: Universal API

Leadfeeder Web Visitors API for reading accounts, tracking setup, feeds, leads, visits, and export jobs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leadfeeder/latest
- **Category:** Marketing
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.leadfeeder.com/
- **Vendor API docs:** https://docs.leadfeeder.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Accounts](actions/get-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Lead Visits](actions/get-lead-visits.md) | GET | Retrieves visits for a lead in Leadfeeder by date range. |
| [Get Visits](actions/get-visits.md) | GET | Retrieves visits for an account in Leadfeeder by date range. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download Feed Report](actions/download-feed-report.md) | GET | Retrieves a feed export report from Leadfeeder. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Get Leads For Custom Feed](actions/get-custom-feed-leads.md) | GET | Retrieves leads for a custom feed in Leadfeeder by date range. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a specific lead from Leadfeeder. |
| [Get Leads](actions/get-leads.md) | GET | Retrieves leads for an account in Leadfeeder by date range. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Export Status](actions/get-feed-export-status.md) | GET | Retrieves the status of a feed export in Leadfeeder. |
| [Get Tracking Script](actions/get-tracking-script.md) | GET | Retrieves an account tracking script from Leadfeeder. |
| [Request Feed Export](actions/request-feed-export.md) | POST | Creates a custom feed export request in Leadfeeder. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Feed](actions/get-custom-feed.md) | GET | Retrieves a specific custom feed from Leadfeeder. |
| [Get Custom Feeds](actions/get-custom-feeds.md) | GET | Retrieves custom feeds for an account in Leadfeeder. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves a specific account from Leadfeeder. |
| [Get Accounts](actions/get-accounts.md) | GET | Retrieves accounts the user can access in Leadfeeder. |

