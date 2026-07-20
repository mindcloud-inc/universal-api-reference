# Ninetailed: Native API Reference

A consolidated summary of Ninetailed's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://www.contentful.com/developers/docs/personalization/
- **API base URL:** `https://api.contentful.com`

## Authentication

### Personal Access Token

Use a Contentful Personal Access Token for Contentful Management API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.contentful.com/help/token-management/personal-access-tokens/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.contentful.management.v1+json` |
| `Content-Type` | `application/vnd.contentful.management.v1+json` |

Responses from this API use JSON. Response data is read from `items`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Content Type](actions/activate-content-type.md) | `PUT /spaces/:space_id/environments/:environment_id/content_types/:content_type_id/published` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types/content-type-activation) |
| [Archive Asset](actions/archive-asset.md) | `PUT /spaces/:spaceId/environments/:environmentId/assets/:assetId/archived` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/asset-archiving) |
| [Archive Entry](actions/archive-entry.md) | `PUT /spaces/:spaceId/environments/:environmentId/entries/:entryId/archived` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entry-archiving) |
| [Create Asset](actions/create-asset.md) | `POST /spaces/:space_id/environments/:environment_id/assets` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/assets-collection) |
| [Create Entry](actions/create-entry.md) | `POST /spaces/:space_id/environments/:environment_id/entries` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entries-collection) |
| [Create Environment](actions/create-environment.md) | `PUT /spaces/:space_id/environments/:environment_id` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/environments/environment) |
| [Create Locale](actions/create-locale.md) | `POST /spaces/:space_id/environments/:environment_id/locales` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/locales/locale) |
| [Create Or Update Asset By ID](actions/create-or-update-asset-by-id.md) | `PUT /spaces/:spaceId/environments/:environmentId/assets/:assetId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/asset) |
| [Create Or Update Content Type](actions/create-or-update-content-type.md) | `PUT /spaces/:space_id/environments/:environment_id/content_types/:content_type_id` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types/content-type) |
| [Create Or Update Entry By ID](actions/create-or-update-entry-by-id.md) | `PUT /spaces/:space_id/environments/:environment_id/entries/:entry_id` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entry) |
| [Create Or Update Tag](actions/create-or-update-tag.md) | `PUT /spaces/:spaceId/environments/:environmentId/tags/:tagId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/tags/tag) |
| [Create Or Update Webhook](actions/create-or-update-webhook.md) | `PUT /spaces/:spaceId/webhook_definitions/:webhookDefinitionId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/webhooks/webhook) |
| [Delete Content Type](actions/delete-content-type.md) | `DELETE /spaces/:spaceId/environments/:environmentId/content_types/:contentTypeId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types/content-type) |
| [Delete Entry](actions/delete-entry.md) | `DELETE /spaces/:spaceId/environments/:environmentId/entries/:entryId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entry) |
| [Delete Environment](actions/delete-environment.md) | `DELETE /spaces/:spaceId/environments/:environmentId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/environments/environment) |
| [Evaluate Profile](actions/evaluate-profile.md) | `POST /v2/organizations/:organizationId/environments/:environmentSlug/profiles` | [docs](https://www.contentful.com/developers/docs/personalization/experience-api/) |
| [Get Asset](actions/get-asset.md) | `GET /spaces/:space_id/environments/:environment_id/assets/:asset_id` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/asset) |
| [Get Content Type](actions/get-content-type.md) | `GET /spaces/:space_id/environments/:environment_id/content_types/:content_type_id` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types/content-type) |
| [Get Entry](actions/get-entry.md) | `GET /spaces/:space_id/environments/:environment_id/entries/:entry_id` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entry) |
| [Get Environment](actions/get-environment.md) | `GET /spaces/:space_id/environments/:environment_id` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/environments/environment) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:organization_id` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/organizations/organization) |
| [Get Space](actions/get-space.md) | `GET /spaces/:space_id` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/spaces/space) |
| [List Assets](actions/list-assets.md) | `GET /spaces/:space_id/environments/:environment_id/assets` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/assets-collection) |
| [List Content Types](actions/list-content-types.md) | `GET /spaces/:space_id/environments/:environment_id/content_types` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/content-types/content-type-collection) |
| [List Entries](actions/list-entries.md) | `GET /spaces/:space_id/environments/:environment_id/entries` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entries-collection) |
| [List Environments](actions/list-environments.md) | `GET /spaces/:space_id/environments` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/environments/environment-collection) |
| [List Locales](actions/list-locales.md) | `GET /spaces/:space_id/environments/:environment_id/locales` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/locales/locale-collection) |
| [List Organization Spaces](actions/list-organization-spaces.md) | `GET /organizations/:organizationId/spaces` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/organizations/organizations-collection) |
| [List Published Entries](actions/list-published-entries.md) | `GET /spaces/:space_id/environments/:environment_id/public/entries` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/published-entries-collection) |
| [List Roles](actions/list-roles.md) | `GET /spaces/:spaceId/roles` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/roles/roles-collection) |
| [List Tags](actions/list-tags.md) | `GET /spaces/:spaceId/environments/:environmentId/tags` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/tags/tag-collection) |
| [List Webhooks](actions/list-webhooks.md) | `GET /spaces/:spaceId/webhook_definitions` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/webhooks/webhooks-collection) |
| [Patch Entry](actions/patch-entry.md) | `PATCH /spaces/:spaceId/environments/:environmentId/entries/:entryId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entry) |
| [Process Asset](actions/process-asset.md) | `PUT /spaces/:spaceId/environments/:environmentId/assets/:assetId/files/:locale/process` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/asset-processing) |
| [Publish Asset](actions/publish-asset.md) | `PUT /spaces/:spaceId/environments/:environmentId/assets/:assetId/published` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/asset-publishing) |
| [Publish Entry](actions/publish-entry.md) | `PUT /spaces/:spaceId/environments/:environmentId/entries/:entryId/published` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entry-publishing) |
| [Unarchive Entry](actions/unarchive-entry.md) | `DELETE /spaces/:spaceId/environments/:environmentId/entries/:entryId/archived` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entry-archiving) |
| [Unpublish Asset](actions/unpublish-asset.md) | `DELETE /spaces/:spaceId/environments/:environmentId/assets/:assetId/published` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/assets/asset-publishing) |
| [Unpublish Entry](actions/unpublish-entry.md) | `DELETE /spaces/:spaceId/environments/:environmentId/entries/:entryId/published` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/entries/entry-publishing) |
| [Update Locale](actions/update-locale.md) | `PUT /spaces/:spaceId/environments/:environmentId/locales/:localeId` | [docs](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/locales/locale) |
