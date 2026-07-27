# Google Search Console: Native API Reference

A consolidated summary of Google Search Console's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/webmaster-tools/v1/api_reference_index
- **API base URL:** `https://www.googleapis.com/webmasters/v3`

## Authentication

### OAuth 2.0

OAuth 2.0 user authorization for Google Search Console.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/webmasters`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/webmaster-tools/v1/how-tos/authorizing)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `rowLimit` in the request body to set the page size (default 25000; accepted range 1–25000). Use `startRow` in the request body as the record offset; numbering starts at 0.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Site](actions/add-site.md) | `PUT sites/:siteUrl` | [docs](https://developers.google.com/webmaster-tools/v1/sites/add) |
| [Delete Site](actions/delete-site.md) | `DELETE sites/:siteUrl` | [docs](https://developers.google.com/webmaster-tools/v1/sites/delete) |
| [Delete Sitemap](actions/delete-sitemap.md) | `DELETE sites/:siteUrl/sitemaps/:feedpath` | [docs](https://developers.google.com/webmaster-tools/v1/sitemaps/delete) |
| [Get Site](actions/get-site.md) | `GET sites/:siteUrl` | [docs](https://developers.google.com/webmaster-tools/v1/sites/get) |
| [Get Sitemap](actions/get-sitemap.md) | `GET sites/:siteUrl/sitemaps/:feedpath` | [docs](https://developers.google.com/webmaster-tools/v1/sitemaps/get) |
| [Inspect URL](actions/inspect-url.md) | `POST https://searchconsole.googleapis.com/v1/urlInspection/index:inspect` | [docs](https://developers.google.com/webmaster-tools/v1/urlInspection.index/inspect) |
| [List Sitemaps](actions/list-sitemaps.md) | `GET sites/:siteUrl/sitemaps` | [docs](https://developers.google.com/webmaster-tools/v1/sitemaps/list) |
| [List Sites](actions/list-sites.md) | `GET sites` | [docs](https://developers.google.com/webmaster-tools/v1/sites/list) |
| [Query Search Analytics](actions/query-search-analytics.md) | `POST sites/:siteUrl/searchAnalytics/query` | [docs](https://developers.google.com/webmaster-tools/v1/searchanalytics/query) |
| [Submit Sitemap](actions/submit-sitemap.md) | `PUT sites/:siteUrl/sitemaps/:feedpath` | [docs](https://developers.google.com/webmaster-tools/v1/sitemaps/submit) |
