# Makeswift: Native API Reference

A consolidated summary of Makeswift's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://docs.makeswift.com/developer/reference/api/overview
- **API base URL:** `https://api.makeswift.com`

## Authentication

### API Key Header

Authenticate by sending your Makeswift App API key in the x-api-key header only.

### Credentials

- **API Key:** `apiKey` · required · Paste your Makeswift App API key (used in x-api-key header).

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.makeswift.com/developer/reference/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `startingAfter` in the query string as the pagination cursor.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Locale](actions/create-locale.md) | `POST /v2/locales` | [docs](https://docs.makeswift.com/developer/reference/api/locales/create-locale) |
| [Create Page](actions/create-page.md) | `POST /v6/pages` | [docs](https://docs.makeswift.com/developer/reference/api/pages/create-page) |
| [Create Route](actions/create-route.md) | `POST /v2/routes` | [docs](https://docs.makeswift.com/developer/reference/api/routes/create-route) |
| [Create Site](actions/create-site.md) | `POST /v2/sites` | [docs](https://docs.makeswift.com/developer/reference/api/sites/create-site) |
| [Delete Locale](actions/delete-locale.md) | `DELETE /v2/locales/:localeIdOrCode` | [docs](https://docs.makeswift.com/developer/reference/api/locales/delete-locale) |
| [Delete Page](actions/delete-page.md) | `DELETE /v6/pages/:pageIdOrPathname` | [docs](https://docs.makeswift.com/developer/reference/api/pages/delete-page) |
| [Delete Route](actions/delete-route.md) | `DELETE /v2/routes/:routeIdOrPathname` | [docs](https://docs.makeswift.com/developer/reference/api/routes/delete-route) |
| [Delete Site](actions/delete-site.md) | `DELETE /v2/sites/:siteId` | [docs](https://docs.makeswift.com/developer/reference/api/sites/delete-site) |
| [Duplicate Site](actions/duplicate-site.md) | `POST /v2/sites/:siteId/duplicate` | [docs](https://docs.makeswift.com/developer/reference/api/sites/duplicate-site) |
| [Get Locale](actions/get-locale.md) | `GET /v2/locales/:localeIdOrCode` | [docs](https://docs.makeswift.com/developer/reference/api/locales/get-locale) |
| [Get Page](actions/get-page.md) | `GET /v6/pages/:pageIdOrPathname` | [docs](https://docs.makeswift.com/developer/reference/api/pages/get-page) |
| [Get Route](actions/get-route.md) | `GET /v2/routes/:routeIdOrPathname` | [docs](https://docs.makeswift.com/developer/reference/api/routes/get-route) |
| [Get Site](actions/get-site.md) | `GET /v2/sites/:siteId` | [docs](https://docs.makeswift.com/developer/reference/api/sites/get-site) |
| [List Locales](actions/list-locales.md) | `GET /v2/locales` | [docs](https://docs.makeswift.com/developer/reference/api/locales/list-locales) |
| [List Pages](actions/list-pages.md) | `GET /v6/pages` | [docs](https://docs.makeswift.com/developer/reference/api/pages/list-pages) |
| [List Routes](actions/list-routes.md) | `GET /v2/routes` | [docs](https://docs.makeswift.com/developer/reference/api/routes/list-routes) |
| [List Sites](actions/list-sites.md) | `GET /v2/sites` | [docs](https://docs.makeswift.com/developer/reference/api/sites/list-sites) |
| [Restore Locale](actions/restore-locale.md) | `POST /v2/locales/:localeIdOrCode/restore` | [docs](https://docs.makeswift.com/developer/reference/api/locales/restore-locale) |
| [Update Locale](actions/update-locale.md) | `PATCH /v2/locales/:localeIdOrCode` | [docs](https://docs.makeswift.com/developer/reference/api/locales/update-locale) |
| [Update Page](actions/update-page.md) | `PATCH /v6/pages/:pageIdOrPathname` | [docs](https://docs.makeswift.com/developer/reference/api/pages/update-page) |
| [Update Route](actions/update-route.md) | `PATCH /v2/routes/:routeIdOrPathname` | [docs](https://docs.makeswift.com/developer/reference/api/routes/update-route) |
| [Update Site](actions/update-site.md) | `PATCH /v2/sites/:siteId` | [docs](https://docs.makeswift.com/developer/reference/api/sites/update-site) |
