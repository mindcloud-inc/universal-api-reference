# Memento Database: Native API Reference

A consolidated summary of Memento Database's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://mementodatabase.docs.apiary.io/
- **API base URL:** `https://api.mementodatabase.com/v1`

## Authentication

### API Key

Use a Memento Cloud API access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://mementodatabase.docs.apiary.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `libraries`.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Entry](actions/create-entry.md) | `POST /libraries/[:libraryId]/entries` | [docs](https://mementodatabase.docs.apiary.io/#reference/0/entries/create-a-new-entry) |
| [Delete Entry](actions/delete-entry.md) | `DELETE /libraries/[:libraryId]/entries/[:entryId]` | [docs](https://mementodatabase.docs.apiary.io/) |
| [Get Entry](actions/get-entry.md) | `GET /libraries/[:libraryId]/entries/[:entryId]` | [docs](https://mementodatabase.docs.apiary.io/#reference/0/entry/get-a-single-entry) |
| [Get Library](actions/get-library.md) | `GET /libraries/[:libraryId]` | [docs](https://mementodatabase.docs.apiary.io/#reference/0/libraries/get-a-library) |
| [List Entries](actions/list-entries.md) | `GET /libraries/[:libraryId]/entries` | [docs](https://mementodatabase.docs.apiary.io/#reference/0/entries/list-entries-on-a-library) |
| [List Libraries](actions/list-libraries.md) | `GET /libraries` | [docs](https://mementodatabase.docs.apiary.io/#reference/0/libraries/list-libraries) |
| [Update Entry](actions/update-entry.md) | `PATCH /libraries/[:libraryId]/entries/[:entryId]` | [docs](https://mementodatabase.docs.apiary.io/#reference/0/entry/edit-an-entry) |
