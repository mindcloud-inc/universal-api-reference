# Restdb.io: Native API Reference

A consolidated summary of Restdb.io's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://restdb.io/media/restdb-cheat-sheet.pdf
- **API base URL:** `https://mindcloudstage0-7934.restdb.io`

## Authentication

### API Key

Provide a Restdb.io database API key. The runtime sends it as the x-apikey header on every request.

### Credentials

- **API Key:** `apiKey` · required · Database API key from the Restdb.io API tools page for the target database.

Send these headers with each API request:

```http
x-apikey: <apiKey>
```

[Official authentication documentation](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Pagination

Use `max` in the query string to set the page size (default 100; accepted range 1–1000). Use `skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `dir`. Use `1` for ascending order and `-1` for descending order. Multiple sort fields can be combined.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Aggregate Documents](actions/aggregate-documents.md) | `GET /rest/:collection` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Bulk Create Documents](actions/bulk-create-documents.md) | `POST /rest/:collection` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Bulk Delete Documents](actions/bulk-delete-documents.md) | `DELETE /rest/:collection/*` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Count Documents](actions/count-documents.md) | `GET /rest/:collection` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Create Child Document](actions/create-child-document.md) | `POST /rest/:collection/:documentId/:childField` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Create Document](actions/create-document.md) | `POST /rest/:collection` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Delete Document](actions/delete-document.md) | `DELETE /rest/:collection/:documentId` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Delete Documents By Query](actions/delete-documents-by-query.md) | `DELETE /rest/:collection/*` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Delete Media](actions/delete-media.md) | `DELETE /media/:mediaId` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Generate JWT](actions/generate-jwt.md) | `POST /auth/jwt` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Get Child Document](actions/get-child-document.md) | `GET /rest/:collection/:documentId/:childField/:childDocumentId` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Get Child Documents](actions/get-child-documents.md) | `GET /rest/:collection/:documentId/:childField` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Get Collection Metadata](actions/get-collection-metadata.md) | `GET /rest/:collection/_meta` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Get Database Metadata](actions/get-database-metadata.md) | `GET /rest/_meta` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Get Document](actions/get-document.md) | `GET /rest/:collection/:documentId` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Get Document References](actions/get-document-references.md) | `GET /rest/:collection/:documentId` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Get Media Metadata](actions/get-media-metadata.md) | `GET /media/:mediaId/meta` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Get User Info](actions/get-user-info.md) | `GET /auth/userinfo` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Group Documents](actions/group-documents.md) | `GET /rest/:collection` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [List Documents](actions/list-documents.md) | `GET /rest/:collection` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [List Documents Flattened](actions/list-documents-flattened.md) | `GET /rest/:collection` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [List Documents With Children](actions/list-documents-with-children.md) | `GET /rest/:collection` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [List Documents With Linked References](actions/list-documents-with-linked-references.md) | `GET /rest/:collection` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [List Documents With Media Data](actions/list-documents-with-media-data.md) | `GET /rest/:collection` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [List Documents With Meta Fields](actions/list-documents-with-meta-fields.md) | `GET /rest/:collection` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [List Documents With Totals](actions/list-documents-with-totals.md) | `GET /rest/:collection` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Logout User](actions/logout-user.md) | `POST /auth/logout` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Patch Document](actions/patch-document.md) | `PATCH /rest/:collection/:documentId` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Replace Document](actions/replace-document.md) | `PUT /rest/:collection/:documentId` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Search Documents](actions/search-documents.md) | `GET /rest/:collection` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Send Email](actions/send-email.md) | `POST /mail` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
| [Upload Media](actions/upload-media.md) | `POST /media` | [docs](https://restdb.io/media/restdb-cheat-sheet.pdf) |
