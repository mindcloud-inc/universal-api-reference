# Rulebricks: Native API Reference

A consolidated summary of Rulebricks's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://rulebricks.com/docs/api-reference
- **OpenAPI specification:** https://rulebricks.com/api/v1/openapi.json
- **API base URL:** `https://rulebricks.com/api/v1`

## Authentication

### API Key

Authenticate Rulebricks API requests with an API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://rulebricks.com/docs/getting-started/integration)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Context](actions/create-context.md) | `POST /admin/contexts` | [docs](https://rulebricks.com/docs/api-reference) |
| [Create or Update Folder](actions/create-or-update-folder.md) | `POST /admin/folders` | [docs](https://rulebricks.com/docs/api-reference) |
| [Create Rule Test](actions/create-rule-test.md) | `POST /admin/rules/:slug/tests` | [docs](https://rulebricks.com/docs/api-reference) |
| [Delete Context](actions/delete-context.md) | `DELETE /admin/contexts/:id` | [docs](https://rulebricks.com/docs/api-reference) |
| [Delete Dynamic Value](actions/delete-dynamic-value.md) | `DELETE /values` | [docs](https://rulebricks.com/docs/api-reference) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /admin/folders` | [docs](https://rulebricks.com/docs/api-reference) |
| [Delete Rule](actions/delete-rule.md) | `DELETE /admin/rules/delete` | [docs](https://rulebricks.com/docs/api-reference) |
| [Delete Rule Test](actions/delete-rule-test.md) | `DELETE /admin/rules/:slug/tests/:testId` | [docs](https://rulebricks.com/docs/api-reference) |
| [Export Rule](actions/export-rule.md) | `GET /admin/rules/export` | [docs](https://rulebricks.com/docs/api-reference) |
| [Get Context](actions/get-context.md) | `GET /admin/contexts/:id` | [docs](https://rulebricks.com/docs/api-reference) |
| [Import Rule](actions/import-rule.md) | `POST /admin/rules/import` | [docs](https://rulebricks.com/docs/api-reference) |
| [List Contexts](actions/list-contexts.md) | `GET /admin/contexts` | [docs](https://rulebricks.com/docs/api-reference) |
| [List Dynamic Values](actions/list-dynamic-values.md) | `GET /values` | [docs](https://rulebricks.com/docs/api-reference) |
| [List Folders](actions/list-folders.md) | `GET /admin/folders` | [docs](https://rulebricks.com/docs/api-reference) |
| [List Rule Tests](actions/list-rule-tests.md) | `GET /admin/rules/:slug/tests` | [docs](https://rulebricks.com/docs/api-reference) |
| [List Rules](actions/list-rules.md) | `GET /admin/rules/list` | [docs](https://rulebricks.com/docs/api-reference) |
| [Solve Rule](actions/solve-rule.md) | `POST /solve/:slug` | [docs](https://rulebricks.com/docs/api-reference) |
| [Update Context](actions/update-context.md) | `PUT /admin/contexts/:id` | [docs](https://rulebricks.com/docs/api-reference) |
| [Update or Add Dynamic Values](actions/update-or-add-dynamic-values.md) | `POST /values` | [docs](https://rulebricks.com/docs/api-reference) |
