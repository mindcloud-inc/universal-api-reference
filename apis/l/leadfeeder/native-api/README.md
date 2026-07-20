# Leadfeeder: Native API Reference

A consolidated summary of Leadfeeder's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://docs.leadfeeder.com/api/
- **API base URL:** `https://api.leadfeeder.com`

## Authentication

### API Key

Connect with a Leadfeeder API token and an API account ID.

### Credentials

- **API Key:** `apiKey` · required
- **Account ID:** `accountId` · required · Leadfeeder API account ID to use for account-scoped endpoints.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.leadfeeder.com/api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `User-Agent` | `MindCloud` |

Responses from this API use JSON.

## Pagination

Use `page[size]` in the query string to set the page size (default 10; accepted range 1–100). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Download Feed Report](actions/download-feed-report.md) | `GET /download/:uniqueFilename` | [docs](https://docs.leadfeeder.com/api/#downloading-the-report) |
| [Get Account](actions/get-account.md) | `GET /accounts/:accountId` | [docs](https://docs.leadfeeder.com/api/#get-a-specific-account) |
| [Get Accounts](actions/get-accounts.md) | `GET /accounts` | [docs](https://docs.leadfeeder.com/api/#get-accounts-the-user-has-access-to) |
| [Get Custom Feed](actions/get-custom-feed.md) | `GET /accounts/:accountId/custom-feeds/:customFeedId` | [docs](https://docs.leadfeeder.com/api/#get-a-specific-custom-feed) |
| [Get Leads For Custom Feed](actions/get-custom-feed-leads.md) | `GET /accounts/:accountId/custom-feeds/:customFeedId/leads` | [docs](https://docs.leadfeeder.com/api/#get-leads-for-custom-feed) |
| [Get Custom Feeds](actions/get-custom-feeds.md) | `GET /accounts/:accountId/custom-feeds` | [docs](https://docs.leadfeeder.com/api/#get-custom-feeds-list-for-an-account) |
| [Get Feed Export Status](actions/get-feed-export-status.md) | `GET /export-requests/:exportRequestId` | [docs](https://docs.leadfeeder.com/api/#feed-export-status) |
| [Get Lead](actions/get-lead.md) | `GET /accounts/:accountId/leads/:leadId` | [docs](https://docs.leadfeeder.com/api/#get-a-specific-lead) |
| [Get Lead Visits](actions/get-lead-visits.md) | `GET /accounts/:accountId/leads/:leadId/visits` | [docs](https://docs.leadfeeder.com/api/#get-all-visits-of-a-lead) |
| [Get Leads](actions/get-leads.md) | `GET /accounts/:accountId/leads` | [docs](https://docs.leadfeeder.com/api/#get-leads) |
| [Get Tracking Script](actions/get-tracking-script.md) | `GET /accounts/:accountId/website-tracking-script` | [docs](https://docs.leadfeeder.com/api/#get-tracking-script-for-a-given-account) |
| [Get Visits](actions/get-visits.md) | `GET /accounts/:accountId/visits` | [docs](https://docs.leadfeeder.com/api/#get-all-visits) |
| [Request Feed Export](actions/request-feed-export.md) | `POST /export-requests` | [docs](https://docs.leadfeeder.com/api/#request-a-feed-export) |
