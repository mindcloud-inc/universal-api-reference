# SmartSuite: Native API Reference

A consolidated summary of SmartSuite's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://developers.smartsuite.com/docs/intro
- **API base URL:** `https://app.smartsuite.com/api/v1`

## Authentication

### API Key

Connect with a SmartSuite API token and workspace ID.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace ID:** `accountId` · required · Your SmartSuite workspace ID, used in the ACCOUNT-ID header.

Send these headers with each API request:

```http
ACCOUNT-ID: <accountId>
```

[Official authentication documentation](https://developers.smartsuite.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; maximum 1000). Use `offset` in the query string as the record offset.

## Filtering

Send filters in the request body.

## Sorting

Set the sort field with `sort` in the request body. Multiple sort fields can be combined.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | `POST /comments/` | [docs](https://developers.smartsuite.com/docs/solution-data/comments/add-comment) |
| [Add Field](actions/add-field.md) | `POST /applications/:tableId/add_field/` | [docs](https://developers.smartsuite.com/docs/solution-data/fields/add-field) |
| [Attach File](actions/attach-file.md) | `PATCH /applications/:tableId/records/:recordId/` | [docs](https://developers.smartsuite.com/docs/solution-data/records/attach-file) |
| [Bulk Add Records](actions/bulk-add-records.md) | `POST /applications/:table_id/records/bulk/` | [docs](https://developers.smartsuite.com/docs/solution-data/records/bulk-add-records) |
| [Bulk Delete Records](actions/bulk-delete-records.md) | `PATCH /applications/:tableId/records/bulk_delete/` | [docs](https://developers.smartsuite.com/docs/solution-data/records/bulk-delete-records) |
| [Bulk Update Records](actions/bulk-update-records.md) | `PATCH /applications/:table_id/records/bulk/` | [docs](https://developers.smartsuite.com/docs/solution-data/records/bulk-update-records) |
| [Create Record](actions/create-record.md) | `POST /applications/:table_id/records/` | [docs](https://developers.smartsuite.com/docs/solution-data/records/create-record) |
| [Create Solution](actions/create-solution.md) | `POST /solutions/` | [docs](https://developers.smartsuite.com/docs/solution-data/solutions/create-solution) |
| [Create Table](actions/create-table.md) | `POST /applications/` | [docs](https://developers.smartsuite.com/docs/solution-data/tables/create-table) |
| [Create View](actions/create-view.md) | `POST /reports/` | [docs](https://developers.smartsuite.com/docs/solution-data/views/create-view) |
| [Create Webhook](actions/create-webhook.md) | `POST https://webhooks.smartsuite.com/smartsuite.webhooks.engine.Webhooks/CreateWebhook` | [docs](https://developers.smartsuite.com/docs/solution-data/webhooks/create-webhook) |
| [Delete Field](actions/delete-field.md) | `POST /applications/:tableId/delete_field/` | [docs](https://developers.smartsuite.com/docs/solution-data/fields/delete-field) |
| [Delete Record](actions/delete-record.md) | `DELETE /applications/:table_id/records/:record_id/` | [docs](https://developers.smartsuite.com/docs/solution-data/records/delete-record) |
| [Duplicate Solution](actions/duplicate-solution.md) | `POST /solutions/duplicate/` | [docs](https://developers.smartsuite.com/docs/solution-data/solutions/duplicate-solution) |
| [Get File URL](actions/get-file-url.md) | `GET /shared-files/:fileHandle/url/` | [docs](https://developers.smartsuite.com/docs/solution-data/records/get-file-url) |
| [Get Record](actions/get-record.md) | `GET /applications/:table_id/records/:record_id/` | [docs](https://developers.smartsuite.com/docs/solution-data/records/get-record) |
| [Get Records For View](actions/get-records-for-view.md) | `GET /applications/:tableId/records-for-report/` | [docs](https://developers.smartsuite.com/docs/solution-data/views/records-for-view) |
| [Get Solution](actions/get-solution.md) | `GET /solutions/:solutionId/` | [docs](https://developers.smartsuite.com/docs/solution-data/solutions/get-solution) |
| [Get Table](actions/get-table.md) | `GET /applications/:table_id/` | [docs](https://developers.smartsuite.com/docs/solution-data/tables/get-table) |
| [Get Webhook](actions/get-webhook.md) | `POST https://webhooks.smartsuite.com/smartsuite.webhooks.engine.Webhooks/GetWebhook` | [docs](https://developers.smartsuite.com/docs/solution-data/webhooks/get-webhook) |
| [List Comments](actions/list-comments.md) | `GET /comments/` | [docs](https://developers.smartsuite.com/docs/solution-data/comments/list-comments) |
| [List Deleted Records](actions/list-deleted-records.md) | `POST /deleted-records/` | [docs](https://developers.smartsuite.com/docs/solution-data/records/list-deleted-records) |
| [List Solutions](actions/list-solutions.md) | `GET /solutions` | [docs](https://developers.smartsuite.com/docs/schemas/solution/list-solutions) |
| [List Tables](actions/list-tables.md) | `GET /applications/` | [docs](https://developers.smartsuite.com/docs/solution-data/tables/list-tables) |
| [List Webhooks](actions/list-webhooks.md) | `POST https://webhooks.smartsuite.com/smartsuite.webhooks.engine.Webhooks/ListWebhooks` | [docs](https://developers.smartsuite.com/docs/solution-data/webhooks/list-webhooks) |
| [Restore Deleted Record](actions/restore-deleted-record.md) | `POST /deleted-records/:recordId/restore/` | [docs](https://developers.smartsuite.com/docs/solution-data/records/restore-deleted-record) |
| [Update Field](actions/update-field.md) | `PUT /applications/:tableId/change_field/` | [docs](https://developers.smartsuite.com/docs/solution-data/fields/update-field) |
| [Update Record](actions/update-record.md) | `PATCH /applications/:table_id/records/:record_id/` | [docs](https://developers.smartsuite.com/docs/solution-data/records/update-record) |
