# Dealfront: Native API Reference

A consolidated summary of Dealfront's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://docs.leadfeeder.com/api/
- **API base URL:** `https://api.leadfeeder.com`

## Authentication

### API Token

Use your Dealfront Leadfeeder API token. MindCloud sends it in the Authorization header required by Leadfeeder.

### Credentials

- **API Token:** `apiKey` · required · Leadfeeder API token from Settings > Personal > API Tokens.

[Official authentication documentation](https://docs.leadfeeder.com/api/#authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `User-Agent` | `MindCloud` |

Responses from this API use JSON.

## Pagination

Use `page[size]` in the query string to set the page size (default 10; accepted range 1–100). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Download Feed Report](actions/download-feed-report.md) | `GET /download/:download_file_name` | [docs](https://docs.leadfeeder.com/api/#downloading-the-report) |
| [Get Account](actions/get-account.md) | `GET /accounts/:account_id` | [docs](https://docs.leadfeeder.com/api/#get-a-specific-account) |
| [Get Custom Feed](actions/get-custom-feed.md) | `GET /accounts/:account_id/custom-feeds/:custom_feed_id` | [docs](https://docs.leadfeeder.com/api/#get-a-specific-custom-feed) |
| [Get Feed Export Status](actions/get-feed-export-status.md) | `GET /export-requests/:id` | [docs](https://docs.leadfeeder.com/api/#feed-export-status) |
| [Get Lead](actions/get-lead.md) | `GET /accounts/:account_id/leads/:lead_id` | [docs](https://docs.leadfeeder.com/api/#get-a-specific-lead) |
| [Get Website Tracking Script](actions/get-website-tracking-script.md) | `GET /accounts/:account_id/website-tracking-script` | [docs](https://docs.leadfeeder.com/api/#get-tracking-script-for-a-given-account) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://docs.leadfeeder.com/api/#get-accounts-the-user-has-access-to) |
| [List Custom Feed Leads](actions/list-custom-feed-leads.md) | `GET /accounts/:account_id/custom-feeds/:custom_feed_id/leads` | [docs](https://docs.leadfeeder.com/api/#get-leads-for-custom-feed) |
| [List Custom Feeds](actions/list-custom-feeds.md) | `GET /accounts/:account_id/custom-feeds` | [docs](https://docs.leadfeeder.com/api/#get-custom-feeds-list-for-an-account) |
| [List Lead Visits](actions/list-lead-visits.md) | `GET /accounts/:account_id/leads/:lead_id/visits` | [docs](https://docs.leadfeeder.com/api/#get-all-visits-of-a-lead) |
| [List Leads](actions/list-leads.md) | `GET /accounts/:account_id/leads` | [docs](https://docs.leadfeeder.com/api/#get-leads) |
| [List Visits](actions/list-visits.md) | `GET /accounts/:account_id/visits` | [docs](https://docs.leadfeeder.com/api/#get-all-visits) |
| [Request Feed Export](actions/request-feed-export.md) | `POST /export-requests` | [docs](https://docs.leadfeeder.com/api/#request-a-feed-export) |
