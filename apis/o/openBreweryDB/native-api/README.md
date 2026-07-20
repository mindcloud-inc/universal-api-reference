# Open Brewery DB: Native API Reference

A consolidated summary of Open Brewery DB's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://openbrewerydb.org/documentation
- **API base URL:** `https://api.openbrewerydb.org/v1`

## Authentication

### No authentication

Open Brewery DB is a free public API and does not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://www.openbrewerydb.org/faq)

## API conventions

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 50; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Brewery](actions/get-brewery.md) | `GET /breweries/:id` | [docs](https://www.openbrewerydb.org/documentation#single-brewery) |
| [Get Brewery Metadata](actions/get-brewery-metadata.md) | `GET /breweries/meta` | [docs](https://www.openbrewerydb.org/documentation#metadata) |
| [List Breweries](actions/list-breweries.md) | `GET /breweries` | [docs](https://www.openbrewerydb.org/documentation#list-breweries) |
| [List Random Breweries](actions/list-random-breweries.md) | `GET /breweries/random` | [docs](https://www.openbrewerydb.org/documentation#random-brewery) |
| [Search Breweries](actions/search-breweries.md) | `GET /breweries/search` | [docs](https://www.openbrewerydb.org/documentation#search-breweries) |
