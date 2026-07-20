# Dub: Native API Reference

A consolidated summary of Dub's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://dub.co/docs/api-reference/introduction
- **API base URL:** `https://api.dub.co`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.dub.co/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.dub.co/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `links.read links.write tags.read tags.write analytics.read domains.read domains.write folders.read folders.write user.read`.

PKCE is enabled. The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.dub.co/oauth/token.

[Official authentication documentation](https://dub.co/docs/integrations/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `pageSize` in the query string to set the page size (default 50; maximum 50). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortOrder`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Create Links](actions/bulk-create-links.md) | `POST /links/bulk` | [docs](https://dub.co/docs/api-reference/links/bulk-create) |
| [Bulk Delete Links](actions/bulk-delete-links.md) | `DELETE /links/bulk` | [docs](https://dub.co/docs/api-reference/links/bulk-delete) |
| [Bulk Update Links](actions/bulk-update-links.md) | `PATCH /links/bulk` | [docs](https://dub.co/docs/api-reference/links/bulk-update) |
| [Check Domain Availability](actions/check-domain-availability.md) | `GET /domains/status` | [docs](https://dub.co/docs/api-reference/domains/check-availability) |
| [Count Links](actions/count-links.md) | `GET /links/count` | [docs](https://dub.co/docs/api-reference/links/count) |
| [Create Link](actions/create-link.md) | `POST /links` | [docs](https://dub.co/docs/api-reference/links/create) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://dub.co/docs/api-reference/tags/create) |
| [Delete Link](actions/delete-link.md) | `DELETE /links/:linkId` | [docs](https://dub.co/docs/api-reference/links/delete) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/:id` | [docs](https://dub.co/docs/api-reference/introduction) |
| [Get QR Code](actions/get-qr-code.md) | `GET /qr` | [docs](https://dub.co/docs/api-reference/endpoint/retrieve-a-qr-code) |
| [Get User Info](actions/get-user-info.md) | `GET /oauth/userinfo` | [docs](https://dub.co/docs/integrations/quickstart) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://dub.co/docs/api-reference/introduction) |
| [List Links](actions/list-links.md) | `GET /links` | [docs](https://dub.co/docs/api-reference/links/list) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://dub.co/docs/api-reference/tags/list) |
| [Retrieve Link](actions/retrieve-link.md) | `GET /links/info` | [docs](https://dub.co/docs/api-reference/links/retrieve) |
| [Update Link](actions/update-link.md) | `PATCH /links/:linkId` | [docs](https://dub.co/docs/api-reference/links/update) |
| [Update Tag](actions/update-tag.md) | `PATCH /tags/:id` | [docs](https://dub.co/docs/api-reference/tags/update) |
| [Upsert Link](actions/upsert-link.md) | `PUT /links/upsert` | [docs](https://dub.co/docs/api-reference/links/upsert) |
