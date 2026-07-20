# SchoolDigger: Native API Reference

A consolidated summary of SchoolDigger's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://developer.schooldigger.com/docs
- **OpenAPI specification:** https://api.schooldigger.com/swagger/docs/v2.3
- **API base URL:** `https://api.schooldigger.com/v2.3`

## Authentication

### API Key

Authenticate requests with SchoolDigger appID and appKey query parameters.

### Credentials

- **API Key:** `apiKey` · required
- **App ID:** `appId` · required · Your SchoolDigger application ID.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.schooldigger.com/docs)

## Pagination

Use `perPage` in the query string to set the page size (default 10; accepted range 1–50). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sortBy` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete Districts](actions/autocomplete-districts.md) | `GET /autocomplete/districts` | [docs](https://developer.schooldigger.com/llms-full.txt) |
| [Autocomplete Schools](actions/autocomplete-schools.md) | `GET /autocomplete/schools` | [docs](https://developer.schooldigger.com/llms-full.txt) |
| [Get District](actions/get-district.md) | `GET /districts/:id` | [docs](https://developer.schooldigger.com/llms-full.txt) |
| [Get School](actions/get-school.md) | `GET /schools/:id` | [docs](https://developer.schooldigger.com/llms-full.txt) |
| [List District Rankings](actions/list-district-rankings.md) | `GET /rankings/districts/:st` | [docs](https://developer.schooldigger.com/llms-full.txt) |
| [List School Rankings](actions/list-school-rankings.md) | `GET /rankings/schools/:st` | [docs](https://developer.schooldigger.com/llms-full.txt) |
| [Search Districts](actions/search-districts.md) | `GET /districts` | [docs](https://developer.schooldigger.com/llms-full.txt) |
| [Search Schools](actions/search-schools.md) | `GET /schools` | [docs](https://developer.schooldigger.com/llms-full.txt) |
