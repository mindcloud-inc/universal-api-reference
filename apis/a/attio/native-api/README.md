# Attio: Native API Reference

A consolidated summary of Attio's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.attio.com/rest-api/endpoint-reference
- **OpenAPI specification:** https://api.attio.com/openapi/api
- **API base URL:** `https://api.attio.com`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.attio.com/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://app.attio.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `user_management:read record_permission:read-write object_configuration:read-write list_entry:read-write list_configuration:read-write comment:read-write note:read-write task:read-write meeting:read-write call_recording:read-write webhook:read-write file:read-write`.

[Official authentication documentation](https://docs.attio.com/rest-api/tutorials/connect-an-app-through-oauth)

### API Token

Use an Attio API key for single-workspace access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.attio.com/rest-api/guides/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assert List Entry by Parent](actions/assert-list-entry-by-parent.md) | `PUT /v2/lists/:list/entries` | [docs](https://docs.attio.com/rest-api/endpoint-reference/entries/assert-a-list-entry-by-parent) |
| [Assert Record](actions/assert-record.md) | `PUT /v2/objects/:object/records` | [docs](https://docs.attio.com/rest-api/endpoint-reference/records/assert-a-record) |
| [Create Entry](actions/create-entry.md) | `POST /v2/lists/:list/entries` | [docs](https://docs.attio.com/rest-api/endpoint-reference/entries/create-an-entry-add-record-to-list) |
| [Create Note](actions/create-note.md) | `POST /v2/notes` | [docs](https://docs.attio.com/rest-api/endpoint-reference/notes/create-a-note) |
| [Create Task](actions/create-task.md) | `POST /v2/tasks` | [docs](https://docs.attio.com/rest-api/endpoint-reference/tasks/create-a-task) |
| [Create Webhook](actions/create-webhook.md) | `POST /v2/webhooks` | [docs](https://docs.attio.com/rest-api/endpoint-reference/webhooks/create-a-webhook) |
| [Delete List Entry](actions/delete-list-entry.md) | `DELETE /v2/lists/:list/entries/:entry_id` | [docs](https://docs.attio.com/rest-api/endpoint-reference/entries/delete-a-list-entry) |
| [Delete Record](actions/delete-record.md) | `DELETE /v2/objects/:object/records/:record_id` | [docs](https://docs.attio.com/rest-api/endpoint-reference/records/delete-a-record) |
| [Get List](actions/get-list.md) | `GET /v2/lists/:list` | [docs](https://docs.attio.com/rest-api/endpoint-reference/lists/get-a-list) |
| [Get List Entry](actions/get-list-entry.md) | `GET /v2/lists/:list/entries/:entry_id` | [docs](https://docs.attio.com/rest-api/endpoint-reference/entries/get-a-list-entry) |
| [Get Object](actions/get-object.md) | `GET /v2/objects/:object` | [docs](https://docs.attio.com/rest-api/endpoint-reference/objects/get-an-object) |
| [Get Record](actions/get-record.md) | `GET /v2/objects/:object/records/:record_id` | [docs](https://docs.attio.com/rest-api/endpoint-reference/records/get-a-record) |
| [Get Task](actions/get-task.md) | `GET /v2/tasks/:task_id` | [docs](https://docs.attio.com/rest-api/endpoint-reference/tasks/get-a-task) |
| [List All Lists](actions/list-all-lists.md) | `GET /v2/lists` | [docs](https://docs.attio.com/rest-api/endpoint-reference/lists/list-all-lists) |
| [List Entries](actions/list-entries.md) | `POST /v2/lists/:list/entries/query` | [docs](https://docs.attio.com/rest-api/endpoint-reference/entries/query-list-entries) |
| [List Notes](actions/list-notes.md) | `GET /v2/notes` | [docs](https://docs.attio.com/rest-api/endpoint-reference/notes/list-notes) |
| [List Objects](actions/list-objects.md) | `GET /v2/objects` | [docs](https://docs.attio.com/rest-api/endpoint-reference/objects/list-objects) |
| [List Records](actions/list-records.md) | `POST /v2/objects/:object/records/query` | [docs](https://docs.attio.com/rest-api/endpoint-reference/records/list-records) |
| [List Tasks](actions/list-tasks.md) | `GET /v2/tasks` | [docs](https://docs.attio.com/rest-api/endpoint-reference/tasks/list-tasks) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v2/webhooks` | [docs](https://docs.attio.com/rest-api/endpoint-reference/webhooks/list-webhooks) |
| [Search Records](actions/search-records.md) | `POST /v2/objects/records/search` | [docs](https://docs.attio.com/rest-api/endpoint-reference/records/search-records) |
| [Update List Entry](actions/update-list-entry.md) | `PUT /v2/lists/:list/entries/:entry_id` | [docs](https://docs.attio.com/rest-api/endpoint-reference/entries/update-a-list-entry-overwrite) |
| [Update Record](actions/update-record.md) | `PUT /v2/objects/:object/records/:record_id` | [docs](https://docs.attio.com/rest-api/endpoint-reference/records/update-a-record-overwrite-multiselect-values) |
| [Update Task](actions/update-task.md) | `PATCH /v2/tasks/:task_id` | [docs](https://docs.attio.com/rest-api/endpoint-reference/tasks/update-a-task) |
