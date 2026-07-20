# Fillout Forms: Native API Reference

A consolidated summary of Fillout Forms's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://www.fillout.com/help/fillout-rest-api
- **REST API base URL:** `https://api.fillout.com/v1/api`
- **REST API base URL:** `https://tables.fillout.com/api/v1`

## Authentication

### OAuth2

Connect via Fillout OAuth2 authorization flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://build.fillout.com/authorize/oauth to approve access.
2. Exchange the returned authorization code with a POST request to https://server.fillout.com/public/oauth/accessToken.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `mc_scope`.

[Official authentication documentation](https://support.fillout.com/help/oauth-applications)

### API Key

Connect via Fillout API key bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.fillout.com/help/api-reference-overview)

## API conventions

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `pageCount`.

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

- **REST API:** Use `limit` in the query string to set the page size (default 50; accepted range 1–150). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

- **REST API:** Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | `POST https://tables.fillout.com/api/v1/bases` | [docs](https://www.fillout.com/help/database/create-database) |
| [Create Database Webhook](actions/create-database-webhook.md) | `POST https://tables.fillout.com/api/v1/bases/:databaseId/webhooks` | [docs](https://www.fillout.com/help/database/create-webhook) |
| [Create Field](actions/create-field.md) | `POST https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/fields` | [docs](https://www.fillout.com/help/database/create-field) |
| [Create Record](actions/create-record.md) | `POST https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records` | [docs](https://www.fillout.com/help/database/create-record) |
| [Create Submissions](actions/create-submissions.md) | `POST /forms/:formId/submissions` | [docs](https://www.fillout.com/help/api-reference/create-submissions) |
| [Create Table](actions/create-table.md) | `POST https://tables.fillout.com/api/v1/bases/:databaseId/tables` | [docs](https://www.fillout.com/help/database/create-table) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhook/create` | [docs](https://www.fillout.com/help/api-reference/create-a-webhook) |
| [Delete Database](actions/delete-database.md) | `DELETE https://tables.fillout.com/api/v1/bases/:databaseId` | [docs](https://www.fillout.com/help/database/delete-database) |
| [Delete Database Webhook](actions/delete-database-webhook.md) | `DELETE https://tables.fillout.com/api/v1/bases/:databaseId/webhooks/:webhookId` | [docs](https://www.fillout.com/help/database/delete-webhook) |
| [Delete Field](actions/delete-field.md) | `DELETE https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/fields/:fieldId` | [docs](https://www.fillout.com/help/database/delete-field) |
| [Delete Record](actions/delete-record.md) | `DELETE https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId` | [docs](https://www.fillout.com/help/database/delete-record) |
| [Delete Submission by ID](actions/delete-submission-by-id.md) | `DELETE /forms/:formId/submissions/:submissionId` | [docs](https://www.fillout.com/help/api-reference/delete-submission-by-id) |
| [Delete Table](actions/delete-table.md) | `DELETE https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId` | [docs](https://www.fillout.com/help/database/delete-table) |
| [Get Database by ID](actions/get-database-by-id.md) | `GET https://tables.fillout.com/api/v1/bases/:databaseId` | [docs](https://www.fillout.com/help/database/get-database-by-id) |
| [Get Form Metadata](actions/get-form-metadata.md) | `GET /forms/:formId` | [docs](https://www.fillout.com/help/api-reference/get-form-metadata) |
| [Get Record by ID](actions/get-record-by-id.md) | `GET https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId` | [docs](https://www.fillout.com/help/database/get-record-by-id) |
| [Get Submission by ID](actions/get-submission-by-id.md) | `GET /forms/:formId/submissions/:submissionId` | [docs](https://www.fillout.com/help/api-reference/get-submission-by-id) |
| [List Database Webhooks](actions/list-database-webhooks.md) | `GET https://tables.fillout.com/api/v1/bases/:databaseId/webhooks` | [docs](https://www.fillout.com/help/database/list-webhooks) |
| [List Databases](actions/list-databases.md) | `GET https://tables.fillout.com/api/v1/bases` | [docs](https://www.fillout.com/help/database/get-databases) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://www.fillout.com/help/api-reference/get-forms) |
| [List Records](actions/list-records.md) | `POST https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/list` | [docs](https://www.fillout.com/help/database/list-records) |
| [List Submissions](actions/list-submissions.md) | `GET /forms/:formId/submissions` | [docs](https://www.fillout.com/help/api-reference/get-all-submissions) |
| [Remove Webhook](actions/remove-webhook.md) | `POST /webhook/delete` | [docs](https://www.fillout.com/help/api-reference/remove-a-webhook) |
| [Update Field](actions/update-field.md) | `PATCH https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/fields/:fieldId` | [docs](https://www.fillout.com/help/database/update-field) |
| [Update Record](actions/update-record.md) | `PATCH https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId` | [docs](https://www.fillout.com/help/database/update-record) |
| [Update Table](actions/update-table.md) | `PATCH https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId` | [docs](https://www.fillout.com/help/database/update-table) |
