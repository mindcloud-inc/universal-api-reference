# File.io: Native API Reference

A consolidated summary of File.io's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://www.file.io/developers
- **OpenAPI specification:** https://www.file.io/developers
- **API base URL:** `https://file.io`

## Authentication

### No authentication

The core public File.io API endpoints selected for this build do not require provider credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.file.io/developers)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `search`.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | `DELETE /{{key}}` | [docs](https://www.file.io/developers) |
| [Download File](actions/download-file.md) | `GET /{{key}}` | [docs](https://www.file.io/developers) |
| [List Files](actions/list-files.md) | `GET /` | [docs](https://www.file.io/developers) |
| [Replace File](actions/replace-file.md) | `PUT /{{key}}` | [docs](https://www.file.io/developers) |
| [Update File](actions/update-file.md) | `PATCH /{{key}}` | [docs](https://www.file.io/developers) |
| [Upload File](actions/upload-file.md) | `POST /` | [docs](https://www.file.io/developers) |
