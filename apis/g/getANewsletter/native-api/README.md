# Get a Newsletter: Native API Reference

A consolidated summary of Get a Newsletter's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://api.getanewsletter.com/v3/docs/
- **API base URL:** `https://api.getanewsletter.com/v3`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.getanewsletter.com/v3/docs/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `ordering` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | `GET /contacts/` | [docs](https://api.getanewsletter.com/v3/docs/contacts/#get-contacts) |
