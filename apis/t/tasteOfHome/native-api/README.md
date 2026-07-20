# Taste of Home: Native API Reference

A consolidated summary of Taste of Home's API configuration, with links to official documentation.

- **Official docs:** https://developer.wordpress.org/rest-api/
- **API base URL:** `https://www.tasteofhome.com`

## Authentication

### No Authentication

Public read-only Taste of Home content endpoints do not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://developer.wordpress.org/rest-api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `orderby` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.
