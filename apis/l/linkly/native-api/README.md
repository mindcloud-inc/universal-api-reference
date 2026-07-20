# Linkly: Native API Reference

A consolidated summary of Linkly's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://linklyhq.com/support/api
- **API base URL:** `https://app.linklyhq.com/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Workspace ID:** `workspace_id` · required · The Linkly workspace ID from the API Access section, used in request paths.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://linklyhq.com/support/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `total_pages`. The current page number is read from `page_number`.

## Pagination

Use `page_size` in the query string to set the page size (default 1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_dir`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Link](actions/create-link.md) | `POST /link` | [docs](https://linklyhq.com/support/link-shortening-api) |
| [Delete Link](actions/delete-link.md) | `DELETE /workspace/:workspace_id/links/:id` | [docs](https://linklyhq.com/support/link-shortening-api) |
| [Export Links](actions/export-links.md) | `GET /workspace/:workspace_id/links/export` | [docs](https://linklyhq.com/support/link-shortening-api) |
| [Get Click Analytics](actions/get-click-analytics.md) | `GET /workspace/:workspace_id/clicks` | [docs](https://linklyhq.com/support/analytics-api) |
| [Get Click Counts Grouped By Dimension](actions/get-click-counts-grouped-by-dimension.md) | `GET /workspace/:workspace_id/clicks/counters/:counter` | [docs](https://linklyhq.com/support/analytics-api) |
| [Get Link](actions/get-link.md) | `GET /link/:id` | [docs](https://linklyhq.com/support/link-shortening-api) |
| [List Links](actions/list-links.md) | `GET /workspace/:workspace_id/list_links` | [docs](https://linklyhq.com/support/link-shortening-api) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://linklyhq.com/support/api) |
| [Update Link](actions/update-link.md) | `POST /link` | [docs](https://linklyhq.com/support/link-shortening-api) |
