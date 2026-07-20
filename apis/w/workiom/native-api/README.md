# Workiom: Native API Reference

A consolidated summary of Workiom's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.workiom.com/swagger/
- **OpenAPI specification:** https://api.workiom.com/swagger/v1/swagger.json
- **API base URL:** `https://api.workiom.com`

## Authentication

### API Key

Workiom API key authentication using the X-Api-Key request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://help.workiom.com/article/workiom-api-guide)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `maxResultCount` in the request body to set the page size (accepted range 1–10000). Use `skipCount` in the request body as the record offset; numbering starts at 0.

## Filtering

Send filters in the request body. Supported operators: `between`, `contain`, `empty`, `eq`, `gt`, `gte`, `includes`, `lt`, `lte`, `ncontain`, `ne`, `nempty`, `notIn`.

## Sorting

Set the sort field with `sorting` in the request body. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | `POST /api/services/app/Fields/Create` | [docs](https://api.workiom.com/swagger/) |
| [Create List](actions/create-list.md) | `POST /api/services/app/Lists/Create` | [docs](https://api.workiom.com/swagger/) |
| [Create Record](actions/create-record.md) | `POST /api/services/app/Data/Create` | [docs](https://api.workiom.com/swagger/) |
| [Create View](actions/create-view.md) | `POST /api/services/app/Views/Create` | [docs](https://api.workiom.com/swagger/) |
| [Delete Record](actions/delete-record.md) | `DELETE /api/services/app/Data/Delete` | [docs](https://api.workiom.com/swagger/) |
| [Get App](actions/get-app.md) | `GET /api/services/app/Apps/Get` | [docs](https://api.workiom.com/swagger/) |
| [Get App Records Count](actions/get-app-records-count.md) | `GET /api/services/app/Data/GetAppRecordsCount` | [docs](https://api.workiom.com/swagger/) |
| [Get Field](actions/get-field.md) | `GET /api/services/app/Fields/Get` | [docs](https://api.workiom.com/swagger/) |
| [Get List](actions/get-list.md) | `GET /api/services/app/Lists/Get` | [docs](https://api.workiom.com/swagger/) |
| [Get Record](actions/get-record.md) | `GET /api/services/app/Data/Get` | [docs](https://api.workiom.com/swagger/) |
| [Get Summary](actions/get-summary.md) | `GET /api/services/app/Data/GetSummary` | [docs](https://api.workiom.com/swagger/) |
| [Get View](actions/get-view.md) | `GET /api/services/app/Views/Get` | [docs](https://api.workiom.com/swagger/) |
| [List Apps](actions/list-apps.md) | `GET /api/services/app/Apps/GetAll` | [docs](https://api.workiom.com/swagger/) |
| [List Fields](actions/list-fields.md) | `GET /api/services/app/Fields/GetAll` | [docs](https://api.workiom.com/swagger/) |
| [List Lists](actions/list-lists.md) | `GET /api/services/app/Lists/GetAll` | [docs](https://api.workiom.com/swagger/) |
| [List Records](actions/list-records.md) | `POST /api/services/app/Data/All` | [docs](https://api.workiom.com/swagger/) |
| [List Records by Field Value](actions/list-records-by-field-value.md) | `GET /api/services/app/Data/GetByFieldValue` | [docs](https://api.workiom.com/swagger/) |
| [List Records With Dependency](actions/list-records-with-dependency.md) | `POST /api/services/app/Data/AllWithDependency` | [docs](https://api.workiom.com/swagger/) |
| [List Views](actions/list-views.md) | `GET /api/services/app/Views/GetAll` | [docs](https://api.workiom.com/swagger/) |
| [Lookup Records](actions/lookup-records.md) | `POST /api/services/app/Data/Lookup` | [docs](https://api.workiom.com/swagger/) |
| [Update Field](actions/update-field.md) | `PUT /api/services/app/Fields/Update` | [docs](https://api.workiom.com/swagger/) |
| [Update List](actions/update-list.md) | `PUT /api/services/app/Lists/Update` | [docs](https://api.workiom.com/swagger/) |
| [Update Record](actions/update-record.md) | `PUT /api/services/app/Data/UpdatePartial` | [docs](https://api.workiom.com/swagger/) |
| [Update View](actions/update-view.md) | `PUT /api/services/app/Views/Update` | [docs](https://api.workiom.com/swagger/) |
