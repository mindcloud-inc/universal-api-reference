# Saleshandy: Native API Reference

A consolidated summary of Saleshandy's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developer.saleshandy.com/
- **OpenAPI specification:** https://developer.saleshandy.com/openapi.json
- **API base URL:** `https://open-api.saleshandy.com/v1`

## Authentication

### API Key

Authenticate Saleshandy with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://developer.saleshandy.com/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `pageSize` in the query string to set the page size (default 100; maximum 1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sort`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Sequence](actions/create-sequence.md) | `POST /sequences` | [docs](https://developer.saleshandy.com/) |
| [Get Credits](actions/get-credits.md) | `GET /credits` | [docs](https://developer.saleshandy.com/) |
| [Get DNC List Items](actions/get-dnc-list-items.md) | `GET /dnc/[:dncListId]` | [docs](https://developer.saleshandy.com/) |
| [Get Enrich Rate Limits](actions/get-enrich-rate-limits.md) | `GET /enrich/rate-limits` | [docs](https://developer.saleshandy.com/) |
| [Get Prospect Minimal Sequences](actions/get-prospect-minimal-sequences.md) | `GET /prospects/[:contactId]/minimal/sequences` | [docs](https://developer.saleshandy.com/) |
| [Get Prospect Verification Status](actions/get-prospect-verification-status.md) | `POST /prospects/verification-status` | [docs](https://developer.saleshandy.com/) |
| [Get Sequence Settings](actions/get-sequence-settings.md) | `GET /sequences/[:sequenceId]/settings` | [docs](https://developer.saleshandy.com/) |
| [Get Sequence Stats](actions/get-sequence-stats.md) | `POST /analytics/stats` | [docs](https://developer.saleshandy.com/) |
| [Get Sequence Step Variants](actions/get-sequence-step-variants.md) | `GET /sequences/[:sequenceId]/steps/[:stepId]` | [docs](https://developer.saleshandy.com/) |
| [Get Task Counts](actions/get-task-counts.md) | `GET /tasks/counts` | [docs](https://developer.saleshandy.com/) |
| [List DNC Lists](actions/list-dnc-lists.md) | `GET /dnc` | [docs](https://developer.saleshandy.com/) |
| [List Fields](actions/list-fields.md) | `GET /fields` | [docs](https://developer.saleshandy.com/) |
| [List Prospect Tags](actions/list-prospect-tags.md) | `GET /prospects/tags` | [docs](https://developer.saleshandy.com/) |
| [List Prospects](actions/list-prospects.md) | `GET /prospects` | [docs](https://developer.saleshandy.com/) |
| [List Schedules](actions/list-schedules.md) | `GET /schedules` | [docs](https://developer.saleshandy.com/) |
| [List Sequence Steps](actions/list-sequence-steps.md) | `GET /sequences/[:sequenceId]/steps` | [docs](https://developer.saleshandy.com/) |
| [List Sequences](actions/list-sequences.md) | `GET /sequences` | [docs](https://developer.saleshandy.com/api-reference/sequences/list) |
| [List Team Members](actions/list-team-members.md) | `GET /user/team-member-list` | [docs](https://developer.saleshandy.com/) |
| [Search DNC Items](actions/search-dnc-items.md) | `GET /dnc/item/search` | [docs](https://developer.saleshandy.com/) |
| [Update Sequence Schedule](actions/update-sequence-schedule.md) | `PATCH /sequences/[:sequenceId]/schedule` | [docs](https://developer.saleshandy.com/) |
