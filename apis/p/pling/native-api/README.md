# Pling: Native API Reference

A consolidated summary of Pling's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://www.opendesktop.org/ocs-api
- **API base URL:** `https://api.pling.com/ocs/v1`

## Authentication

### No authentication

Pling's public OCS read endpoints are accessible without authentication. The supplied image did not include a password or API key, and Pling's account check endpoint rejected the username-only check.

This API does not require request authentication.

[Official authentication documentation](https://www.opendesktop.org/ocs-api)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `pagesize` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sortmode` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get API Configuration](actions/get-api-configuration.md) | `GET /config` | [docs](https://www.opendesktop.org/ocs-api) |
| [Get Content](actions/get-content.md) | `GET /content/data/:contentId` | [docs](https://www.opendesktop.org/ocs-api) |
| [Get Content Download](actions/get-content-download.md) | `GET /content/download/:contentId/:itemId` | [docs](https://www.opendesktop.org/ocs-api) |
| [List Content](actions/list-content.md) | `GET /content/data` | [docs](https://www.opendesktop.org/ocs-api) |
| [List Content By Category](actions/list-content-by-category.md) | `GET /content/data` | [docs](https://www.opendesktop.org/ocs-api) |
| [List Content By User](actions/list-content-by-user.md) | `GET /content/data` | [docs](https://www.opendesktop.org/ocs-api) |
| [List Content Categories](actions/list-content-categories.md) | `GET /content/categories` | [docs](https://www.opendesktop.org/ocs-api) |
| [List Content Comments](actions/list-content-comments.md) | `GET /comments/data/:type/:contentId/:contentId2` | [docs](https://www.opendesktop.org/ocs-api) |
| [List Popular Content](actions/list-popular-content.md) | `GET /content/data` | [docs](https://www.opendesktop.org/ocs-api) |
| [Search Content](actions/search-content.md) | `GET /content/data` | [docs](https://www.opendesktop.org/ocs-api) |
