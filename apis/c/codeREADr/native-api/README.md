# CodeREADr: Native API Reference

A consolidated summary of CodeREADr's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://secure.codereadr.com/apidocs/
- **API base URL:** `https://api.codereadr.com`

## Authentication

### CodeREADr API Key

Connect with a CodeREADr API key for the Developer API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://secure.codereadr.com/apidocs/README.md#finding)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/xml` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use XML.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Question to Service](actions/add-question-to-service.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Services.md#add) |
| [Authorize User for Service](actions/authorize-user-for-service.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Services.md#authorize) |
| [Bulk Upsert Database Values](actions/bulk-upsert-database-values.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Databases.md#upsertmultivalue) |
| [Clear Database](actions/clear-database.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Databases.md#clear) |
| [Create Database](actions/create-database.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Databases.md#create) |
| [Create Question](actions/create-question.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Questions.md#create) |
| [Create Service](actions/create-service.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Services.md#create) |
| [Create User](actions/create-user.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Users.md#create) |
| [Delete Database](actions/delete-database.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Databases.md#delete) |
| [Delete Database Value](actions/delete-database-value.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Databases.md#deletevalue) |
| [Delete Service](actions/delete-service.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Services.md#delete) |
| [Delete User](actions/delete-user.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Users.md#delete) |
| [List Database Values](actions/list-database-values.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Databases.md#showvalues) |
| [List Databases](actions/list-databases.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Databases.md#retrieve) |
| [List Questions](actions/list-questions.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Questions.md#retrieve) |
| [List Scans](actions/list-scans.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Scans.md#retrieve) |
| [List Services](actions/list-services.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Services.md#retrieve) |
| [List Users](actions/list-users.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Users.md#retrieve) |
| [Retrieve Limits](actions/retrieve-limits.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Limits.md#retrieve) |
| [Revoke User from Service](actions/revoke-user-from-service.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Services.md#authorize) |
| [Update Database](actions/update-database.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Databases.md#update) |
| [Update Service](actions/update-service.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Services.md#edit) |
| [Update User](actions/update-user.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Users.md#edit) |
| [Upsert Database Value](actions/upsert-database-value.md) | `POST /api/` | [docs](https://secure.codereadr.com/apidocs/Databases.md#upsertvalue) |
