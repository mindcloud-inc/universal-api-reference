# Myphoner: Native API Reference

A consolidated summary of Myphoner's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://www.myphoner.com/docs/api/
- **API base URL:** `https://{subdomain}.myphoner.com/api/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Subdomain:** `subdomain` · required · Your Myphoner workspace subdomain, without .myphoner.com

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://myphoner.help/en/articles/4722143-using-your-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Lead](actions/archive-lead.md) | `POST /leads/:leadId/archive` | [docs](https://www.myphoner.com/docs/api/#leads) |
| [Create Lead](actions/create-lead.md) | `POST /lists/:listId/leads` | [docs](https://www.myphoner.com/docs/api/#leads) |
| [Create List](actions/create-list.md) | `POST /lists` | [docs](https://www.myphoner.com/docs/api/#lists) |
| [Delegate Lead](actions/delegate-lead.md) | `PATCH /leads/:leadId/delegate` | [docs](https://www.myphoner.com/docs/api/#leads) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhook/:webhookId` | [docs](https://www.myphoner.com/docs/api/#webhooks) |
| [Find Leads](actions/find-leads.md) | `GET /lists/:listId/leads/find` | [docs](https://www.myphoner.com/docs/api/#leads) |
| [Get Call Information](actions/get-call-information.md) | `GET /calls/:callId` | [docs](https://www.myphoner.com/docs/api/#calls) |
| [Get Lead](actions/get-lead.md) | `GET /leads/:leadId` | [docs](https://www.myphoner.com/docs/api/#leads) |
| [Get List](actions/get-list.md) | `GET /lists/:listId` | [docs](https://www.myphoner.com/docs/api/#lists) |
| [Get List Statistics](actions/get-list-statistics.md) | `GET /lists/:listId/stats` | [docs](https://www.myphoner.com/docs/api/#lists) |
| [List Columns for List](actions/list-columns-for-list.md) | `GET /lists/:listId/columns` | [docs](https://www.myphoner.com/docs/api/#view-columns) |
| [List Leads in List](actions/list-leads-in-list.md) | `GET /lists/:listId/leads` | [docs](https://www.myphoner.com/docs/api/#lists) |
| [List Lists](actions/list-lists.md) | `GET /lists` | [docs](https://www.myphoner.com/docs/api/#lists) |
| [Mark Lead as Loser](actions/mark-lead-as-loser.md) | `POST /leads/:leadId/loser` | [docs](https://www.myphoner.com/docs/api/#leads) |
| [Mark Lead as Winner](actions/mark-lead-as-winner.md) | `POST /leads/:leadId/winner` | [docs](https://www.myphoner.com/docs/api/#leads) |
| [Mark Lead for Call Back](actions/mark-lead-for-call-back.md) | `POST /leads/:leadId/call_back` | [docs](https://www.myphoner.com/docs/api/#leads) |
| [Migrate Lead](actions/migrate-lead.md) | `PATCH /leads/:leadId/migrate` | [docs](https://www.myphoner.com/docs/api/#leads) |
| [Search Leads](actions/search-leads.md) | `GET /leads/search` | [docs](https://www.myphoner.com/docs/api/#leads) |
| [Update Lead](actions/update-lead.md) | `PATCH /leads/:leadId` | [docs](https://www.myphoner.com/docs/api/#leads) |
