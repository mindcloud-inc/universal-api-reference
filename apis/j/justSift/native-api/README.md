# JustSift: Native API Reference

A consolidated summary of JustSift's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://developers.justsift.com/
- **API base URL:** `https://api.justsift.com/v1`

## Authentication

### Sift API Tokens

Uses a Sift data API token for Bearer requests and a separate media token for media URL access.

### Credentials

- **API Token:** `apiToken` · required · Sift data API token used as the Bearer token for data requests.
- **Media Token:** `mediaToken` · required · Sift media token used for media endpoints and media URLs.

Send these headers with each API request:

```http
Authorization: Bearer <apiToken>
Authorization: Bearer <mediaToken>
```

[Official authentication documentation](https://developers.justsift.com/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 10; accepted range 0–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortDirection`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Advanced People Search](actions/advanced-people-search.md) | `POST /search/people` | [docs](https://developers.justsift.com/) |
| [Get Person](actions/get-person.md) | `GET /people/:idOrEmail` | [docs](https://developers.justsift.com/) |
| [Get Person Media](actions/get-person-media.md) | `GET /media/people/:idOrEmail/:mediaKind` | [docs](https://developers.justsift.com/) |
| [List Person Fields](actions/list-person-fields.md) | `GET /fields/person` | [docs](https://developers.justsift.com/) |
| [Search People](actions/search-people.md) | `GET /search/people` | [docs](https://developers.justsift.com/) |
