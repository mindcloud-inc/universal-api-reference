# Extruct AI: Native API Reference

A consolidated summary of Extruct AI's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.extruct.ai/api-reference/introduction
- **API base URL:** `https://api.extruct.ai`

## Authentication

### API Key

Bearer token generated in the Extruct AI dashboard API Tokens page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.extruct.ai/api-reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Input Data](actions/add-input-data.md) | `POST /v1/tables/:table_id/rows` | [docs](https://docs.extruct.ai/api-reference/tables/create-table-rows) |
| [Clone Table](actions/clone-table.md) | `POST /v1/tables/:table_id/clone` | [docs](https://docs.extruct.ai/api-reference/tables/clone-table) |
| [Create Discovery Task](actions/create-discovery-task.md) | `POST /v1/discovery_tasks` | [docs](https://docs.extruct.ai/api-reference/discover/create-company-discovery-task) |
| [Create Table](actions/create-table.md) | `POST /v1/tables` | [docs](https://docs.extruct.ai/api-reference/tables/create-table) |
| [Create Table Columns](actions/create-table-columns.md) | `POST /v1/tables/:table_id/columns` | [docs](https://docs.extruct.ai/api-reference/tables/create-table-columns) |
| [Delete Table](actions/delete-table.md) | `DELETE /v1/tables/:table_id` | [docs](https://docs.extruct.ai/api-reference/tables/delete-table) |
| [Delete Table Column](actions/delete-table-column.md) | `DELETE /v1/tables/:table_id/columns/:column_id` | [docs](https://docs.extruct.ai/api-reference/tables/delete-table-column) |
| [Delete Table Rows](actions/delete-table-rows.md) | `DELETE /v1/tables/:table_id/rows` | [docs](https://docs.extruct.ai/api-reference/tables/delete-table-rows) |
| [Find Similar Companies](actions/find-similar-companies.md) | `GET /v1/companies/:company_identifier/similar` | [docs](https://docs.extruct.ai/api-reference/lookalike-search) |
| [Get Discovery Task](actions/get-discovery-task.md) | `GET /v1/discovery_tasks/:task_id` | [docs](https://docs.extruct.ai/api-reference/discover/get-company-discovery-task) |
| [Get Discovery Task Results](actions/get-discovery-task-results.md) | `GET /v1/discovery_tasks/:task_id/results` | [docs](https://docs.extruct.ai/api-reference/discover/get-company-discovery-task-results) |
| [Get Row Data](actions/get-row-data.md) | `GET /v1/tables/:table_id/rows/:row_id` | [docs](https://docs.extruct.ai/api-reference/tables/get-table-row) |
| [Get Table](actions/get-table.md) | `GET /v1/tables/:table_id` | [docs](https://docs.extruct.ai/api-reference/tables/get-table) |
| [Get Table Data](actions/get-table-data.md) | `GET /v1/tables/:table_id/data` | [docs](https://docs.extruct.ai/api-reference/tables/get-table-data) |
| [Get User](actions/get-user.md) | `GET /v1/user` | [docs](https://www.extruct.ai/docs/api-reference/user) |
| [Healthcheck](actions/healthcheck.md) | `GET /v1/healthcheck` | [docs](https://docs.extruct.ai/api-reference/healthcheck) |
| [List Discovery Tasks](actions/list-discovery-tasks.md) | `GET /v1/discovery_tasks` | [docs](https://docs.extruct.ai/api-reference/discover/list-company-discovery-tasks) |
| [List Tables](actions/list-tables.md) | `GET /v1/tables` | [docs](https://docs.extruct.ai/api-reference/tables/list-tables) |
| [Resume Discovery Task](actions/resume-discovery-task.md) | `POST /v1/discovery_tasks/:task_id/resume` | [docs](https://docs.extruct.ai/api-reference/discover/resume-company-discovery-task) |
| [Run Enrichment](actions/run-enrichment.md) | `POST /v1/tables/:table_id/run` | [docs](https://docs.extruct.ai/api-reference/tables/run-table) |
| [Search Companies](actions/search-companies.md) | `GET /v1/companies/search` | [docs](https://docs.extruct.ai/api-reference/search) |
| [Update Table](actions/update-table.md) | `PATCH /v1/tables/:table_id` | [docs](https://docs.extruct.ai/api-reference/tables/update-table) |
| [Update Table Column](actions/update-table-column.md) | `PATCH /v1/tables/:table_id/columns/:column_id` | [docs](https://docs.extruct.ai/api-reference/tables/update-table-column) |
| [Update Table Rows](actions/update-table-rows.md) | `PATCH /v1/tables/:table_id/rows` | [docs](https://docs.extruct.ai/api-reference/tables/update-table-rows) |
