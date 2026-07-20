# Harpoon: Native API Reference

A consolidated summary of Harpoon's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://app.harpoonapp.com/api
- **OpenAPI specification:** https://app.harpoonapp.com/api-docs/api-docs.json
- **API base URL:** `https://app.harpoonapp.com/api`

## Authentication

### Personal Access Token

Use a Harpoon personal access token from your Account API page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.harpoonapp.com/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `meta.pagination.last_page`. The current page number is read from `meta.pagination.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 25; maximum 100).

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Clone Time Entry](actions/clone-time-entry.md) | `POST /time_entries/:id/clone` | [docs](https://app.harpoonapp.com/api) |
| [Create Estimate](actions/create-estimate.md) | `POST /estimates` | [docs](https://app.harpoonapp.com/api) |
| [Create Expense](actions/create-expense.md) | `POST /expenses` | [docs](https://app.harpoonapp.com/api) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://app.harpoonapp.com/api) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /time_entries` | [docs](https://app.harpoonapp.com/api) |
| [Delete Time Entry](actions/delete-time-entry.md) | `DELETE /time_entries/:id` | [docs](https://app.harpoonapp.com/api) |
| [Get Client](actions/get-client.md) | `GET /clients/:id` | [docs](https://app.harpoonapp.com/api) |
| [Get Expense](actions/get-expense.md) | `GET /expenses/:id` | [docs](https://app.harpoonapp.com/api) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:id` | [docs](https://app.harpoonapp.com/api) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://app.harpoonapp.com/api) |
| [Get Time Entry](actions/get-time-entry.md) | `GET /time_entries/:id` | [docs](https://app.harpoonapp.com/api) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://app.harpoonapp.com/api) |
| [List Estimates](actions/list-estimates.md) | `GET /estimates` | [docs](https://app.harpoonapp.com/api) |
| [List Expenses](actions/list-expenses.md) | `GET /expenses` | [docs](https://app.harpoonapp.com/api) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://app.harpoonapp.com/api) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://app.harpoonapp.com/api) |
| [List Time Entries](actions/list-time-entries.md) | `GET /time_entries` | [docs](https://app.harpoonapp.com/api) |
| [Update Client](actions/update-client.md) | `PUT /clients/:id` | [docs](https://app.harpoonapp.com/api) |
| [Update Expense](actions/update-expense.md) | `PUT /expenses/:id` | [docs](https://app.harpoonapp.com/api) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:id` | [docs](https://app.harpoonapp.com/api) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://app.harpoonapp.com/api) |
| [Update Time Entry](actions/update-time-entry.md) | `PUT /time_entries/:id` | [docs](https://app.harpoonapp.com/api) |
