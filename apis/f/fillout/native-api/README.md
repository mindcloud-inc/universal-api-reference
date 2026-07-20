# Fillout: Native API Reference

A consolidated summary of Fillout's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://support.fillout.com/help/database/api
- **API base URL:** `https://api.fillout.com/v1/api`

## Authentication

### API Key

Authenticate Fillout API requests with your Fillout API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.fillout.com/help/database/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | `POST https://tables.fillout.com/api/v1/bases` | [docs](https://fillout.com/help/database/api) |
| [Create Database Webhook](actions/create-database-webhook.md) | `POST https://tables.fillout.com/api/v1/bases/:databaseId/webhooks` | [docs](https://fillout.com/help/database/api) |
| [Create Field](actions/create-field.md) | `POST https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/fields` | [docs](https://fillout.com/help/database/api) |
| [Create Form Submission](actions/create-form-submission.md) | `POST /forms/:formId/submissions` | [docs](https://fillout.com/help/api-reference/create-submissions) |
| [Create Form Webhook](actions/create-form-webhook.md) | `POST /webhook/create` | [docs](https://fillout.com/help/api-reference/create-a-webhook) |
| [Create Record](actions/create-record.md) | `POST https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records` | [docs](https://fillout.com/help/database/api) |
| [Create Table](actions/create-table.md) | `POST https://tables.fillout.com/api/v1/bases/:databaseId/tables` | [docs](https://fillout.com/help/database/api) |
| [Delete Database](actions/delete-database.md) | `DELETE https://tables.fillout.com/api/v1/bases/:databaseId` | [docs](https://fillout.com/help/database/api) |
| [Delete Database Webhook](actions/delete-database-webhook.md) | `DELETE https://tables.fillout.com/api/v1/bases/:databaseId/webhooks/:webhookId` | [docs](https://fillout.com/help/database/api) |
| [Delete Field](actions/delete-field.md) | `DELETE https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/fields/:fieldId` | [docs](https://fillout.com/help/database/api) |
| [Delete Form Submission](actions/delete-form-submission.md) | `DELETE /forms/:formId/submissions/:submissionId` | [docs](https://fillout.com/help/api-reference/delete-submission-by-id) |
| [Delete Form Webhook](actions/delete-form-webhook.md) | `POST /webhook/delete` | [docs](https://fillout.com/help/api-reference/remove-a-webhook) |
| [Delete Record](actions/delete-record.md) | `DELETE https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId` | [docs](https://fillout.com/help/database/api) |
| [Delete Table](actions/delete-table.md) | `DELETE https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId` | [docs](https://fillout.com/help/database/api) |
| [Get Database By Id](actions/get-database-by-id.md) | `GET https://tables.fillout.com/api/v1/bases/:databaseId` | [docs](https://fillout.com/help/database/api) |
| [Get Databases](actions/get-databases.md) | `GET https://tables.fillout.com/api/v1/bases` | [docs](https://fillout.com/help/database/api) |
| [Get Form Metadata](actions/get-form-metadata.md) | `GET /forms/:formId` | [docs](https://fillout.com/help/api-reference/get-form-metadata) |
| [Get Form Submission](actions/get-form-submission.md) | `GET /forms/:formId/submissions/:submissionId` | [docs](https://fillout.com/help/api-reference/get-submission-by-id) |
| [Get Record By Id](actions/get-record-by-id.md) | `GET https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId` | [docs](https://fillout.com/help/database/api) |
| [List Database Webhooks](actions/list-database-webhooks.md) | `GET https://tables.fillout.com/api/v1/bases/:databaseId/webhooks` | [docs](https://fillout.com/help/database/api) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /forms/:formId/submissions` | [docs](https://fillout.com/help/api-reference/get-all-submissions) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://fillout.com/help/api-reference/get-forms) |
| [List Records](actions/list-records.md) | `POST https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/list` | [docs](https://fillout.com/help/database/api) |
| [Update Field](actions/update-field.md) | `PATCH https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/fields/:fieldId` | [docs](https://fillout.com/help/database/api) |
| [Update Record](actions/update-record.md) | `PATCH https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId` | [docs](https://fillout.com/help/database/api) |
| [Update Table](actions/update-table.md) | `PATCH https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId` | [docs](https://fillout.com/help/database/api) |
