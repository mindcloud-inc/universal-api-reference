# Kontent.ai: Native API Reference

A consolidated summary of Kontent.ai's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://kontent.ai/learn/docs/apis
- **API base URL:** `https://deliver.kontent.ai`

## Authentication

### Management API key

Authenticate with a Kontent.ai Management API key in the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://kontent.ai/learn/docs/apis/management-api-v2/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `content-type` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment_id` | path | `string` | yes | Identifies the Kontent.ai environment. |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–2000). Use `skip` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `order` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add content type snippet](actions/add-content-type-snippet.md) | `POST https://manage.kontent.ai/v2/projects/:environment_id/snippets` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/content-type-snippets) |
| [Add management asset](actions/add-management-asset.md) | `POST https://manage.kontent.ai/v2/projects/:environment_id/assets` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/assets) |
| [Add management content item](actions/add-management-content-item.md) | `POST https://manage.kontent.ai/v2/projects/:environment_id/items` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/content-items) |
| [Add management language](actions/add-management-language.md) | `POST https://manage.kontent.ai/v2/projects/:environment_id/languages` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/languages) |
| [Add management taxonomy group](actions/add-management-taxonomy-group.md) | `POST https://manage.kontent.ai/v2/projects/:environment_id/taxonomies` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/taxonomy-groups) |
| [Delete content type snippet](actions/delete-content-type-snippet.md) | `DELETE https://manage.kontent.ai/v2/projects/:environment_id/snippets/:snippet_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/content-type-snippets) |
| [Delete management asset](actions/delete-management-asset.md) | `DELETE https://manage.kontent.ai/v2/projects/:environment_id/assets/:asset_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/assets) |
| [Delete management content item](actions/delete-management-content-item.md) | `DELETE https://manage.kontent.ai/v2/projects/:environment_id/items/:item_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/content-items) |
| [Delete management taxonomy group](actions/delete-management-taxonomy-group.md) | `DELETE https://manage.kontent.ai/v2/projects/:environment_id/taxonomies/:taxonomy_group_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/taxonomy-groups) |
| [Enumerate content items](actions/enumerate-content-items.md) | `GET /:environment_id/items-feed` | [docs](https://kontent.ai/learn/docs/apis/delivery-api/content-items) |
| [List content items](actions/list-content-items.md) | `GET /:environment_id/items` | [docs](https://kontent.ai/learn/docs/apis/delivery-api/content-items) |
| [List content type snippets](actions/list-content-type-snippets.md) | `GET https://manage.kontent.ai/v2/projects/:environment_id/snippets` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/content-type-snippets) |
| [List content types](actions/list-content-types.md) | `GET /:environment_id/types` | [docs](https://kontent.ai/learn/docs/apis/delivery-api/content-types) |
| [List custom apps](actions/list-custom-apps.md) | `GET https://manage.kontent.ai/v2/projects/:environment_id/custom-apps` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/custom-apps) |
| [List items referencing asset](actions/list-items-referencing-asset.md) | `GET /:environment_id/assets/:asset_id/used-in` | [docs](https://kontent.ai/learn/docs/apis/delivery-api/content-items) |
| [List items referencing item](actions/list-items-referencing-item.md) | `GET /:environment_id/items/:item_codename/used-in` | [docs](https://kontent.ai/learn/docs/apis/delivery-api/content-items) |
| [List languages](actions/list-languages.md) | `GET /:environment_id/languages` | [docs](https://kontent.ai/learn/docs/apis/delivery-api/languages) |
| [List management assets](actions/list-management-assets.md) | `GET https://manage.kontent.ai/v2/projects/:environment_id/assets` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/assets) |
| [List management collections](actions/list-management-collections.md) | `GET https://manage.kontent.ai/v2/projects/:environment_id/collections` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/collections) |
| [List management content items](actions/list-management-content-items.md) | `GET https://manage.kontent.ai/v2/projects/:environment_id/items` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/content-items) |
| [List management languages](actions/list-management-languages.md) | `GET https://manage.kontent.ai/v2/projects/:environment_id/languages` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/languages) |
| [List management taxonomy groups](actions/list-management-taxonomy-groups.md) | `GET https://manage.kontent.ai/v2/projects/:environment_id/taxonomies` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/taxonomy-groups) |
| [List taxonomy groups](actions/list-taxonomy-groups.md) | `GET /:environment_id/taxonomies` | [docs](https://kontent.ai/learn/docs/apis/delivery-api/taxonomy-groups) |
| [Modify content type snippet](actions/modify-content-type-snippet.md) | `PATCH https://manage.kontent.ai/v2/projects/:environment_id/snippets/:snippet_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/content-type-snippets) |
| [Modify management collections](actions/modify-management-collections.md) | `PATCH https://manage.kontent.ai/v2/projects/:environment_id/collections` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/collections) |
| [Modify management language](actions/modify-management-language.md) | `PATCH https://manage.kontent.ai/v2/projects/:environment_id/languages/:language_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/languages) |
| [Modify management taxonomy group](actions/modify-management-taxonomy-group.md) | `PATCH https://manage.kontent.ai/v2/projects/:environment_id/taxonomies/:taxonomy_group_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/taxonomy-groups) |
| [Retrieve content item](actions/retrieve-content-item.md) | `GET /:environment_id/items/:item_codename` | [docs](https://kontent.ai/learn/docs/apis/delivery-api/content-items) |
| [Retrieve content type](actions/retrieve-content-type.md) | `GET /:environment_id/types/:type_codename` | [docs](https://kontent.ai/learn/docs/apis/delivery-api/content-types) |
| [Retrieve content type element](actions/retrieve-content-type-element.md) | `GET /:environment_id/types/:type_codename/elements/:element_codename` | [docs](https://kontent.ai/learn/docs/apis/delivery-api/content-types) |
| [Retrieve content type snippet](actions/retrieve-content-type-snippet.md) | `GET https://manage.kontent.ai/v2/projects/:environment_id/snippets/:snippet_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/content-type-snippets) |
| [Retrieve custom app](actions/retrieve-custom-app.md) | `GET https://manage.kontent.ai/v2/projects/:environment_id/custom-apps/:custom_app_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/custom-apps) |
| [Retrieve management asset](actions/retrieve-management-asset.md) | `GET https://manage.kontent.ai/v2/projects/:environment_id/assets/:asset_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/assets) |
| [Retrieve management content item](actions/retrieve-management-content-item.md) | `GET https://manage.kontent.ai/v2/projects/:environment_id/items/:item_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/content-items) |
| [Retrieve management language](actions/retrieve-management-language.md) | `GET https://manage.kontent.ai/v2/projects/:environment_id/languages/:language_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/languages) |
| [Retrieve management taxonomy group](actions/retrieve-management-taxonomy-group.md) | `GET https://manage.kontent.ai/v2/projects/:environment_id/taxonomies/:taxonomy_group_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/taxonomy-groups) |
| [Retrieve taxonomy group](actions/retrieve-taxonomy-group.md) | `GET /:environment_id/taxonomies/:taxonomy_group_codename` | [docs](https://kontent.ai/learn/docs/apis/delivery-api/taxonomy-groups) |
| [Upload management asset file](actions/upload-management-asset-file.md) | `POST https://manage.kontent.ai/v2/projects/:environment_id/files/:file_name` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/assets) |
| [Upsert management asset](actions/upsert-management-asset.md) | `PUT https://manage.kontent.ai/v2/projects/:environment_id/assets/external-id/:external_id` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/assets) |
| [Upsert management content item](actions/upsert-management-content-item.md) | `PUT https://manage.kontent.ai/v2/projects/:environment_id/items/:item_identifier` | [docs](https://kontent.ai/learn/docs/apis/management-api-v2/content-items) |
