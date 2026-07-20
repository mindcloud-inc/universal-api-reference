# Felt: Native API Reference

A consolidated summary of Felt's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://developers.felt.com/rest-api/getting-started
- **API base URL:** `https://felt.com/api/v2`

## Authentication

### API Key

Authenticate with a Felt workspace API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.felt.com/rest-api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Layer From Data Source](actions/add-layer-from-data-source.md) | `POST /maps/:mapId/add_source_layer` | [docs](https://developers.felt.com/rest-api/api-reference/layers/layer-uploads) |
| [Check Custom Export Status](actions/check-custom-export-status.md) | `GET /maps/:mapId/layers/:layerId/custom_exports/:exportId` | [docs](https://developers.felt.com/rest-api/api-reference/layers/layer-exports) |
| [Create An Embed Token](actions/create-an-embed-token.md) | `POST /maps/:mapId/embed_token` | [docs](https://developers.felt.com/rest-api/api-reference/embed-tokens) |
| [Create Custom Layer Export](actions/create-custom-layer-export.md) | `POST /maps/:mapId/layers/:layerId/custom_export` | [docs](https://developers.felt.com/rest-api/api-reference/layers/layer-exports) |
| [Create Layer Export Link](actions/create-layer-export-link.md) | `GET /maps/:mapId/layers/:layerId/get_export_link` | [docs](https://developers.felt.com/rest-api/api-reference/layers/layer-exports) |
| [Create Map](actions/create-map.md) | `POST /maps` | [docs](https://developers.felt.com/rest-api/api-reference/maps) |
| [Create Or Update Map Element Groups](actions/create-or-update-map-element-groups.md) | `POST /maps/:mapId/element_groups` | [docs](https://developers.felt.com/rest-api/api-reference/elements) |
| [Create Or Update Map Elements](actions/create-or-update-map-elements.md) | `POST /maps/:mapId/elements` | [docs](https://developers.felt.com/rest-api/api-reference/elements) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://developers.felt.com/rest-api/api-reference/projects) |
| [Create Source](actions/create-source.md) | `POST /sources` | [docs](https://developers.felt.com/rest-api/api-reference/sources) |
| [Delete Map](actions/delete-map.md) | `DELETE /maps/:mapId` | [docs](https://developers.felt.com/rest-api/api-reference/maps) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:projectId` | [docs](https://developers.felt.com/rest-api/api-reference/projects) |
| [Delete Source](actions/delete-source.md) | `DELETE /sources/:sourceId` | [docs](https://developers.felt.com/rest-api/api-reference/sources) |
| [Duplicate Map](actions/duplicate-map.md) | `POST /maps/:mapId/duplicate` | [docs](https://developers.felt.com/rest-api/api-reference/maps) |
| [Duplicate Map Layers](actions/duplicate-map-layers.md) | `POST /duplicate_layers` | [docs](https://developers.felt.com/rest-api/api-reference/layers) |
| [Export Map Comments](actions/export-map-comments.md) | `GET /maps/:mapId/comments/export` | [docs](https://developers.felt.com/rest-api/api-reference/comments) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://developers.felt.com/rest-api/api-reference/users) |
| [Get Map](actions/get-map.md) | `GET /maps/:mapId` | [docs](https://developers.felt.com/rest-api/api-reference/maps) |
| [Get Map Element Group](actions/get-map-element-group.md) | `GET /maps/:mapId/element_groups/:groupId` | [docs](https://developers.felt.com/rest-api/api-reference/elements) |
| [Get Map Layer](actions/get-map-layer.md) | `GET /maps/:mapId/layers/:layerId` | [docs](https://developers.felt.com/rest-api/api-reference/layers) |
| [Get Map Layer Group](actions/get-map-layer-group.md) | `GET /maps/:mapId/layer_groups/:layerGroupId` | [docs](https://developers.felt.com/rest-api/api-reference/layers) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectId` | [docs](https://developers.felt.com/rest-api/api-reference/projects) |
| [Get Source](actions/get-source.md) | `GET /sources/:sourceId` | [docs](https://developers.felt.com/rest-api/api-reference/sources) |
| [List Library Layers](actions/list-library-layers.md) | `GET /library` | [docs](https://developers.felt.com/rest-api/api-reference/layers/layer-library) |
| [List Map Element Groups](actions/list-map-element-groups.md) | `GET /maps/:mapId/element_groups` | [docs](https://developers.felt.com/rest-api/api-reference/elements) |
| [List Map Elements](actions/list-map-elements.md) | `GET /maps/:mapId/elements` | [docs](https://developers.felt.com/rest-api/api-reference/elements) |
| [List Map Layer Groups](actions/list-map-layer-groups.md) | `GET /maps/:mapId/layer_groups` | [docs](https://developers.felt.com/rest-api/api-reference/layers) |
| [List Map Layers](actions/list-map-layers.md) | `GET /maps/:mapId/layers` | [docs](https://developers.felt.com/rest-api/api-reference/layers) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developers.felt.com/rest-api/api-reference/projects) |
| [List Sources](actions/list-sources.md) | `GET /sources` | [docs](https://developers.felt.com/rest-api/api-reference/sources) |
| [Move Map](actions/move-map.md) | `POST /maps/:mapId/move` | [docs](https://developers.felt.com/rest-api/api-reference/maps) |
| [Publish Map Layer](actions/publish-map-layer.md) | `POST /maps/:mapId/layers/:layerId/publish` | [docs](https://developers.felt.com/rest-api/api-reference/layers/layer-library) |
| [Publish Map Layer Group](actions/publish-map-layer-group.md) | `POST /maps/:mapId/layer_groups/:layerGroupId/publish` | [docs](https://developers.felt.com/rest-api/api-reference/layers/layer-library) |
| [Sync Source](actions/sync-source.md) | `POST /sources/:sourceId/sync` | [docs](https://developers.felt.com/rest-api/api-reference/sources) |
| [Update Layer Style](actions/update-layer-style.md) | `POST /maps/:mapId/layers/:layerId/update_style` | [docs](https://developers.felt.com/rest-api/api-reference/layers) |
| [Update Map](actions/update-map.md) | `POST /maps/:mapId/update` | [docs](https://developers.felt.com/rest-api/api-reference/maps) |
| [Update Map Layer](actions/update-map-layer.md) | `POST /maps/:mapId/layers` | [docs](https://developers.felt.com/rest-api/api-reference/layers) |
| [Update Map Layer Group](actions/update-map-layer-group.md) | `POST /maps/:mapId/layer_groups/:layerGroupId` | [docs](https://developers.felt.com/rest-api/api-reference/layers) |
| [Update Project](actions/update-project.md) | `POST /projects/:projectId/update` | [docs](https://developers.felt.com/rest-api/api-reference/projects) |
| [Update Source](actions/update-source.md) | `POST /sources/:sourceId/update` | [docs](https://developers.felt.com/rest-api/api-reference/sources) |
| [Upload Map Layer](actions/upload-map-layer.md) | `POST /maps/:mapId/upload` | [docs](https://developers.felt.com/rest-api/api-reference/layers/layer-uploads) |
