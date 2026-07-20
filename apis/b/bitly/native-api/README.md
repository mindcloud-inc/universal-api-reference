# Bitly: Native API Reference

A consolidated summary of Bitly's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://dev.bitly.com/api-reference/
- **OpenAPI specification:** https://dev.bitly.com/v4/v4.json
- **API base URL:** `https://api-ssl.bitly.com/v4`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://bitly.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api-ssl.bitly.com/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


[Official authentication documentation](https://dev.bitly.com/docs/getting-started/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `size` in the query string to set the page size (default 50).

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Update Group Bitlinks](actions/bulk-update-group-bitlinks.md) | `PATCH /groups/:group_guid/bitlinks` | [docs](https://dev.bitly.com/api-reference#updateBitlinksByGroup) |
| [Create Full Bitlink](actions/create-full-bitlink.md) | `POST /bitlinks` | [docs](https://dev.bitly.com/api-reference#createFullBitlink) |
| [Delete Bitlink](actions/delete-bitlink.md) | `DELETE /bitlinks/:bitlink` | [docs](https://dev.bitly.com/api-reference#deleteBitlink) |
| [Expand Bitlink](actions/expand-bitlink.md) | `POST /expand` | [docs](https://dev.bitly.com/api-reference#expandBitlink) |
| [Get Bitlink](actions/get-bitlink.md) | `GET /bitlinks/:bitlink` | [docs](https://dev.bitly.com/api-reference#getBitlink) |
| [Get Group](actions/get-group.md) | `GET /groups/:group_guid` | [docs](https://dev.bitly.com/api-reference#getGroup) |
| [Get Group Feature Usage](actions/get-group-feature-usage.md) | `GET /groups/:group_guid/feature_usage` | [docs](https://dev.bitly.com/api-reference#getGroupFeatureUsage) |
| [Get Group Preferences](actions/get-group-preferences.md) | `GET /groups/:group_guid/preferences` | [docs](https://dev.bitly.com/api-reference#getGroupPreferences) |
| [Get OAuth App](actions/get-oauth-app.md) | `GET /apps/:client_id` | [docs](https://dev.bitly.com/api-reference#getOAuthApp) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:organization_guid` | [docs](https://dev.bitly.com/api-reference#getOrganization) |
| [Get Organization Plan Limits](actions/get-organization-plan-limits.md) | `GET /organizations/:organization_guid/plan_limits` | [docs](https://dev.bitly.com/api-reference#getPlanLimits) |
| [Get Organization Shorten Counts By Group](actions/get-organization-shorten-counts-by-group.md) | `GET /organizations/:organization_guid/shorten_counts_by_group` | [docs](https://dev.bitly.com/api-reference#getOrganizationShortenCountsByGroup) |
| [Get Platform Limits](actions/get-platform-limits.md) | `GET /user/platform_limits` | [docs](https://dev.bitly.com/api-reference#getPlatformLimits) |
| [Get QR Code](actions/get-qr-code.md) | `GET /qr-codes/:qrcode_id` | [docs](https://dev.bitly.com/api-reference#getQRCodeByIdPublic) |
| [Get QR Code Image](actions/get-qr-code-image.md) | `GET /qr-codes/:qrcode_id/image` | [docs](https://dev.bitly.com/api-reference#getQRCodeImagePublic) |
| [Get Sorted Bitlinks](actions/get-sorted-bitlinks.md) | `GET /groups/:group_guid/bitlinks/:sort` | [docs](https://dev.bitly.com/api-reference#getSortedBitlinks) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://dev.bitly.com/api-reference#getUser) |
| [List BSDs](actions/list-bsds.md) | `GET /bsds` | [docs](https://dev.bitly.com/api-reference#getBSDs) |
| [List Group Bitlinks](actions/list-group-bitlinks.md) | `GET /groups/:group_guid/bitlinks` | [docs](https://dev.bitly.com/api-reference#getBitlinksByGroup) |
| [List Group QR Codes](actions/list-group-qr-codes.md) | `GET /groups/:group_guid/qr-codes` | [docs](https://dev.bitly.com/api-reference#listQRMinimal) |
| [List Group Tags](actions/list-group-tags.md) | `GET /groups/:group_guid/tags` | [docs](https://dev.bitly.com/api-reference#getGroupTags) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://dev.bitly.com/api-reference#getGroups) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://dev.bitly.com/api-reference#getOrganizations) |
| [Shorten Link](actions/shorten-link.md) | `POST /shorten` | [docs](https://dev.bitly.com/api-reference#createBitlink) |
| [Update Bitlink](actions/update-bitlink.md) | `PATCH /bitlinks/:bitlink` | [docs](https://dev.bitly.com/api-reference#updateBitlink) |
| [Update Group](actions/update-group.md) | `PATCH /groups/:group_guid` | [docs](https://dev.bitly.com/api-reference#updateGroup) |
| [Update Group Preferences](actions/update-group-preferences.md) | `PATCH /groups/:group_guid/preferences` | [docs](https://dev.bitly.com/api-reference#updateGroupPreferences) |
| [Update QR Code](actions/update-qr-code.md) | `PATCH /qr-codes/:qrcode_id` | [docs](https://dev.bitly.com/api-reference#updateQRCodePublic) |
