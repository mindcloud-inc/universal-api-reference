# Webling: Native API Reference

A consolidated summary of Webling's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://demo.webling.ch/api/1
- **API base URL:** `https://{instanceDomain}/api/1`

## Authentication

### API Key

Connect using a Webling API key and tenant instance domain.

### Credentials

- **API Key:** `apiKey` · required
- **Instance Domain:** `instanceDomain` · required · Full Webling tenant host, for example yourclub.webling.ch or yourclub.webling.eu.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://demo.webling.ch/api/1#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 100; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `gte`, `lt`, `lte`, `neq`.

## Sorting

Set the sort field with `order` in the query string. Use `ASC` for ascending order and `DESC` for descending order. Multiple sort fields can be combined.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | `POST /document` | [docs](https://demo.webling.ch/api/1#document-document-list-post) |
| [Create Documentgroup](actions/create-documentgroup.md) | `POST /documentgroup` | [docs](https://demo.webling.ch/api/1#documentgroup-documentgroup-list-post) |
| [Create Membergroup](actions/create-membergroup.md) | `POST /membergroup` | [docs](https://demo.webling.ch/api/1#membergroup-membergroup-list-post) |
| [Delete Document](actions/delete-document.md) | `DELETE /document/:id` | [docs](https://demo.webling.ch/api/1#document-document-delete) |
| [Get Changes After Revision](actions/get-changes-after-revision.md) | `GET /replicate/:id` | [docs](https://demo.webling.ch/api/1#track-changes-replicate-get-changes-after-a-revision-get) |
| [Get Changes Since Timestamp](actions/get-changes-since-timestamp.md) | `GET /changes/:timestamp` | [docs](https://demo.webling.ch/api/1#track-changes-replicate-get-changes-since-timestamp-get) |
| [Get Current Revision](actions/get-current-revision.md) | `GET /replicate` | [docs](https://demo.webling.ch/api/1#track-changes-replicate-current-revision-get) |
| [Get Current User](actions/get-current-user.md) | `GET /currentuser` | [docs](https://demo.webling.ch/api/1#currentuser-current-user-get) |
| [Get Document](actions/get-document.md) | `GET /document/:id` | [docs](https://demo.webling.ch/api/1#document-document-get) |
| [Get Document Content](actions/get-document-content.md) | `GET /document/:id/file/:filename.:extension` | [docs](https://demo.webling.ch/api/1#document-document-content-get) |
| [Get Documentgroup](actions/get-documentgroup.md) | `GET /documentgroup/:id` | [docs](https://demo.webling.ch/api/1#documentgroup-documentgroup-get) |
| [List Articles](actions/list-articles.md) | `GET /article` | [docs](https://demo.webling.ch/api/1#article-article-list-get) |
| [List Debitors](actions/list-debitors.md) | `GET /debitor` | [docs](https://demo.webling.ch/api/1#debitor-debitor-list-get) |
| [List Documentgroups](actions/list-documentgroups.md) | `GET /documentgroup` | [docs](https://demo.webling.ch/api/1#documentgroup-documentgroup-list-get) |
| [List Documents](actions/list-documents.md) | `GET /document` | [docs](https://demo.webling.ch/api/1#document-document-list-get) |
| [List Entries](actions/list-entries.md) | `GET /entry` | [docs](https://demo.webling.ch/api/1#entry-entry-list-get) |
| [List Entrygroups](actions/list-entrygroups.md) | `GET /entrygroup` | [docs](https://demo.webling.ch/api/1#entrygroup-entrygroup-list-get) |
| [List Membergroups](actions/list-membergroups.md) | `GET /membergroup` | [docs](https://demo.webling.ch/api/1#membergroup-membergroup-list-get) |
| [List Members](actions/list-members.md) | `GET /member` | [docs](https://demo.webling.ch/api/1#member-member-list-get) |
| [List Users](actions/list-users.md) | `GET /user` | [docs](https://demo.webling.ch/api/1#user-user-list-get) |
| [Update Document](actions/update-document.md) | `PUT /document/:id` | [docs](https://demo.webling.ch/api/1#document-document-put) |
