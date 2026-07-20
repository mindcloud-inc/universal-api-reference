# Data Blaze: Native API Reference

A consolidated summary of Data Blaze's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://blaze.today/datablaze/docs/apis/
- **API base URL:** `https://data-api.blaze.today`

## Authentication

### API Key

Authenticate with a Data Blaze space API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://blaze.today/datablaze/docs/apis/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Table Row](actions/create-table-row.md) | `POST /api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/` | [docs](https://blaze.today/datablaze/docs/apis/) |
| [Delete Table Row](actions/delete-table-row.md) | `DELETE /api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/{rowId}/` | [docs](https://blaze.today/datablaze/docs/apis/) |
| [Get Table Row](actions/get-table-row.md) | `GET /api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/{rowId}/` | [docs](https://blaze.today/datablaze/docs/apis/) |
| [List Accessible Tables](actions/list-accessible-tables.md) | `GET /api/database/tables/all-tables/` | [docs](https://blaze.today/datablaze/docs/apis/) |
| [List Table Fields](actions/list-table-fields.md) | `GET /api/database/fields/table/6S69TxVQg3kaNMphZCdHyV/` | [docs](https://blaze.today/datablaze/docs/apis/) |
| [List Table Rows](actions/list-table-rows.md) | `GET /api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/` | [docs](https://blaze.today/datablaze/docs/apis/) |
| [Move Table Row](actions/move-table-row.md) | `PATCH /api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/{rowId}/move/` | [docs](https://blaze.today/datablaze/docs/apis/) |
| [Run SQL Query](actions/run-sql-query.md) | `POST /api/database/1OzRoKyYgXpIR32FUO1JMm/query/` | [docs](https://blaze.today/datablaze/docs/apis/) |
| [Update Table Row](actions/update-table-row.md) | `PATCH /api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/{rowId}/` | [docs](https://blaze.today/datablaze/docs/apis/) |
