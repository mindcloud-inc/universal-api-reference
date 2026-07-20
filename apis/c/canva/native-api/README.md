# Canva: Native API Reference

A consolidated summary of Canva's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.canva.dev/docs/connect/
- **OpenAPI specification:** https://www.canva.dev/sources/connect/api/latest/api.yml
- **API base URL:** `https://api.canva.com/rest`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.canva.com/api/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.canva.com/rest/v1/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `comment:write brandtemplate:content:read design:permission:read app:read brandtemplate:content:write brandtemplate:meta:read design:content:read app:write folder:write design:permission:write design:content:write design:meta:read folder:read asset:read folder:permission:write comment:read asset:write folder:permission:read profile:read`.

PKCE is enabled. The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.canva.com/rest/v1/oauth/token.

[Official authentication documentation](https://www.canva.dev/docs/connect/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `continuation`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `offset` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Only one sort field is accepted.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Design](actions/create-design.md) | `POST /v1/designs` | [docs](https://www.canva.dev/docs/connect/api-reference/designs/create-design/) |
| [Create Design Export Job](actions/create-design-export-job.md) | `POST /v1/exports` | [docs](https://www.canva.dev/docs/connect/api-reference/exports/create-design-export-job/) |
| [Create Folder](actions/create-folder.md) | `POST /v1/folders` | [docs](https://www.canva.dev/docs/connect/api-reference/folders/create-folder/) |
| [Create URL Asset Upload Job](actions/create-url-asset-upload-job.md) | `POST /v1/url-asset-uploads` | [docs](https://www.canva.dev/docs/connect/api-reference/assets/create-url-asset-upload-job/) |
| [Create URL Import Job](actions/create-url-import-job.md) | `POST /v1/url-imports` | [docs](https://www.canva.dev/docs/connect/api-reference/design-imports/create-url-import-job/) |
| [Get Asset](actions/get-asset.md) | `GET /v1/assets/:assetId` | [docs](https://www.canva.dev/docs/connect/api-reference/assets/get-asset/) |
| [Get Current User](actions/get-current-user.md) | `GET /v1/users/me` | [docs](https://www.canva.dev/docs/connect/api-reference/users/users-me/) |
| [Get Design](actions/get-design.md) | `GET /v1/designs/:designId` | [docs](https://www.canva.dev/docs/connect/api-reference/designs/get-design/) |
| [Get Design Export Formats](actions/get-design-export-formats.md) | `GET /v1/designs/:designId/export-formats` | [docs](https://www.canva.dev/docs/connect/api-reference/designs/get-design-export-formats/) |
| [Get Design Export Job](actions/get-design-export-job.md) | `GET /v1/exports/:exportId` | [docs](https://www.canva.dev/docs/connect/api-reference/exports/get-design-export-job/) |
| [Get Design Pages](actions/get-design-pages.md) | `GET /v1/designs/:designId/pages` | [docs](https://www.canva.dev/docs/connect/api-reference/designs/get-design-pages/) |
| [Get Folder](actions/get-folder.md) | `GET /v1/folders/:folderId` | [docs](https://www.canva.dev/docs/connect/api-reference/folders/get-folder/) |
| [Get URL Asset Upload Job](actions/get-url-asset-upload-job.md) | `GET /v1/url-asset-uploads/:jobId` | [docs](https://www.canva.dev/docs/connect/api-reference/assets/get-url-asset-upload-job/) |
| [Get URL Import Job](actions/get-url-import-job.md) | `GET /v1/url-imports/:jobId` | [docs](https://www.canva.dev/docs/connect/api-reference/design-imports/get-url-import-job/) |
| [Get User Capabilities](actions/get-user-capabilities.md) | `GET /v1/users/me/capabilities` | [docs](https://www.canva.dev/docs/connect/api-reference/users/get-user-capabilities/) |
| [Get User Profile](actions/get-user-profile.md) | `GET /v1/users/me/profile` | [docs](https://www.canva.dev/docs/connect/api-reference/users/users-profile/) |
| [List Designs](actions/list-designs.md) | `GET /v1/designs` | [docs](https://www.canva.dev/docs/connect/api-reference/designs/list-designs/) |
| [List Folder Items](actions/list-folder-items.md) | `GET /v1/folders/:folderId/items` | [docs](https://www.canva.dev/docs/connect/api-reference/folders/list-folder-items/) |
| [Move Folder Item](actions/move-folder-item.md) | `POST /v1/folders/move` | [docs](https://www.canva.dev/docs/connect/api-reference/folders/move-folder-item/) |
| [Update Folder](actions/update-folder.md) | `PATCH /v1/folders/:folderId` | [docs](https://www.canva.dev/docs/connect/api-reference/folders/update-folder/) |
