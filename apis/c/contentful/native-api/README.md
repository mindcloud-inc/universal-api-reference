# Contentful: Native API Reference

A consolidated summary of Contentful's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.contentful.com/developers/docs/references/content-management-api/
- **API base URL:** `https://api.contentful.com`

## Authentication

### Personal Access Token

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.contentful.com/developers/docs/references/authentication/)

### OAuth 2.0

Authenticate with a Contentful OAuth app to access the Content Management API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://be.contentful.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://be.contentful.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `content_management_manage`.

[Official authentication documentation](https://www.contentful.com/developers/docs/references/authentication/#the-content-management-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.contentful.management.v1+json` |
| `Content-Type` | `application/vnd.contentful.management.v1+json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `skip` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `order` in the query string. Multiple sort fields can be combined.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate content type](actions/activate-content-type.md) | `PUT /spaces/:spaceId/environments/:environmentId/content_types/:contentTypeId/published` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types) |
| [Archive asset](actions/archive-asset.md) | `PUT /spaces/:spaceId/environments/:environmentId/assets/:assetId/archived` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets) |
| [Archive entry](actions/archive-entry.md) | `PUT /spaces/:spaceId/environments/:environmentId/entries/:entryId/archived` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries) |
| [Create asset](actions/create-asset.md) | `POST /spaces/:spaceId/environments/:environmentId/assets` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets) |
| [Create content type](actions/create-content-type.md) | `POST /spaces/:spaceId/environments/:environmentId/content_types` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types) |
| [Create content type with ID](actions/create-content-type-with-id.md) | `PUT /spaces/:spaceId/environments/:environmentId/content_types/:contentTypeId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types) |
| [Create entry](actions/create-entry.md) | `POST /spaces/:spaceId/environments/:environmentId/entries` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries) |
| [Create entry with ID](actions/create-entry-with-id.md) | `PUT /spaces/:spaceId/environments/:environmentId/entries/:entryId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries) |
| [Create locale](actions/create-locale.md) | `POST /spaces/:spaceId/environments/:environmentId/locales` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/locales) |
| [Create or update asset](actions/create-or-update-asset.md) | `PUT /spaces/:spaceId/environments/:environmentId/assets/:assetId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets) |
| [Deactivate content type](actions/deactivate-content-type.md) | `DELETE /spaces/:spaceId/environments/:environmentId/content_types/:contentTypeId/published` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types) |
| [Delete asset](actions/delete-asset.md) | `DELETE /spaces/:spaceId/environments/:environmentId/assets/:assetId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets) |
| [Delete content type](actions/delete-content-type.md) | `DELETE /spaces/:spaceId/environments/:environmentId/content_types/:contentTypeId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types) |
| [Delete entry](actions/delete-entry.md) | `DELETE /spaces/:spaceId/environments/:environmentId/entries/:entryId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries) |
| [Delete locale](actions/delete-locale.md) | `DELETE /spaces/:spaceId/environments/:environmentId/locales/:localeId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/locales) |
| [Get asset](actions/get-asset.md) | `GET /spaces/:spaceId/environments/:environmentId/assets/:assetId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets) |
| [Get content type](actions/get-content-type.md) | `GET /spaces/:spaceId/environments/:environmentId/content_types/:contentTypeId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types) |
| [Get entry](actions/get-entry.md) | `GET /spaces/:spaceId/environments/:environmentId/entries/:entryId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries) |
| [Get entry references](actions/get-entry-references.md) | `GET /spaces/:spaceId/environments/:environmentId/entries/:entryId/references` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries) |
| [Get environment](actions/get-environment.md) | `GET /spaces/:spaceId/environments/:environmentId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/environments) |
| [Get environment alias](actions/get-environment-alias.md) | `GET /spaces/:spaceId/environment_aliases/:environmentAliasId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/environment-aliases) |
| [Get locale](actions/get-locale.md) | `GET /spaces/:spaceId/environments/:environmentId/locales/:localeId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/locales) |
| [Get space](actions/get-space.md) | `GET /spaces/:spaceId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/spaces) |
| [List assets](actions/list-assets.md) | `GET /spaces/:spaceId/environments/:environmentId/assets` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets) |
| [List content types](actions/list-content-types.md) | `GET /spaces/:spaceId/environments/:environmentId/content_types` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types) |
| [List entries](actions/list-entries.md) | `GET /spaces/:spaceId/environments/:environmentId/entries` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entries-collection/get-all-entries-of-a-space) |
| [List environment aliases](actions/list-environment-aliases.md) | `GET /spaces/:spaceId/environment_aliases` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/environment-aliases) |
| [List environments](actions/list-environments.md) | `GET /spaces/:spaceId/environments` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/environments) |
| [List locales](actions/list-locales.md) | `GET /spaces/:spaceId/environments/:environmentId/locales` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/locales) |
| [List spaces](actions/list-spaces.md) | `GET /spaces` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/spaces) |
| [Patch entry](actions/patch-entry.md) | `PATCH /spaces/:spaceId/environments/:environmentId/entries/:entryId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries) |
| [Process asset](actions/process-asset.md) | `PUT /spaces/:spaceId/environments/:environmentId/assets/:assetId/files/:localeCode/process` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets) |
| [Publish asset](actions/publish-asset.md) | `PUT /spaces/:spaceId/environments/:environmentId/assets/:assetId/published` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets) |
| [Publish entry](actions/publish-entry.md) | `PUT /spaces/:spaceId/environments/:environmentId/entries/:entryId/published` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries) |
| [Unarchive asset](actions/unarchive-asset.md) | `DELETE /spaces/:spaceId/environments/:environmentId/assets/:assetId/archived` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets) |
| [Unarchive entry](actions/unarchive-entry.md) | `DELETE /spaces/:spaceId/environments/:environmentId/entries/:entryId/archived` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries) |
| [Unpublish asset](actions/unpublish-asset.md) | `DELETE /spaces/:spaceId/environments/:environmentId/assets/:assetId/published` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets) |
| [Unpublish entry](actions/unpublish-entry.md) | `DELETE /spaces/:spaceId/environments/:environmentId/entries/:entryId/published` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries) |
| [Update entry](actions/update-entry.md) | `PUT /spaces/:spaceId/environments/:environmentId/entries/:entryId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries) |
| [Update locale](actions/update-locale.md) | `PUT /spaces/:spaceId/environments/:environmentId/locales/:localeId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/locales) |
