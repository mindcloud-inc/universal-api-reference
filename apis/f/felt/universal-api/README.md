# <img src="https://images.mindcloud.co/apps/icons/felt_1776279397942.png" alt="Felt logo" width="28" height="28"> Felt: Universal API

Create, share, and collaborate on maps

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/felt/latest
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://felt.com
- **Vendor API docs:** https://developers.felt.com/rest-api/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Custom Export Status

| Action | Method | Description |
| --- | --- | --- |
| [Check Custom Export Status](actions/check-custom-export-status.md) | GET | Retrieves custom layer export status from Felt. |

### Custom Layer Export

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Layer Export](actions/create-custom-layer-export.md) | POST | Creates a custom layer export in Felt. |

### Duplicated Layer

| Action | Method | Description |
| --- | --- | --- |
| [Duplicate Map Layers](actions/duplicate-map-layers.md) | POST | Creates duplicated map layers in Felt. |

### Embed Token

| Action | Method | Description |
| --- | --- | --- |
| [Create An Embed Token](actions/create-an-embed-token.md) | POST | Creates a short-lived embed token in Felt. |

### Layer

| Action | Method | Description |
| --- | --- | --- |
| [Add Layer From Data Source](actions/add-layer-from-data-source.md) | POST | Creates a map layer from a data source in Felt. |
| [Get Map Layer](actions/get-map-layer.md) | GET | Retrieves a map layer from Felt. |
| [List Map Layers](actions/list-map-layers.md) | GET | Retrieves map layers from Felt. |
| [Upload Map Layer](actions/upload-map-layer.md) | POST | Uploads a new map layer to Felt. |

### Layer Export Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Layer Export Link](actions/create-layer-export-link.md) | GET | Retrieves a layer export link from Felt. |

### Library Layer

| Action | Method | Description |
| --- | --- | --- |
| [List Library Layers](actions/list-library-layers.md) | GET | Retrieves library layers from Felt. |

### Map

| Action | Method | Description |
| --- | --- | --- |
| [Create Map](actions/create-map.md) | POST | Creates a new map in Felt. |
| [Delete Map](actions/delete-map.md) | DELETE | Deletes an existing map from Felt. |
| [Duplicate Map](actions/duplicate-map.md) | POST | Creates a duplicate of a map in Felt. |
| [Get Map](actions/get-map.md) | GET | Retrieves a map from Felt. |
| [Move Map](actions/move-map.md) | PUT | Moves a map to another location in Felt. |
| [Update Map](actions/update-map.md) | PUT | Updates an existing map in Felt. |

### Map Comment

| Action | Method | Description |
| --- | --- | --- |
| [Export Map Comments](actions/export-map-comments.md) | GET | Retrieves exported map comments from Felt. |

### Map Element

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Map Elements](actions/create-or-update-map-elements.md) | PUT | Creates or updates map elements in Felt. |
| [List Map Elements](actions/list-map-elements.md) | GET | Retrieves map elements from Felt. |

### Map Element Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Map Element Groups](actions/create-or-update-map-element-groups.md) | PUT | Creates or updates map element groups in Felt. |
| [Get Map Element Group](actions/get-map-element-group.md) | GET | Retrieves a map element group from Felt. |
| [List Map Element Groups](actions/list-map-element-groups.md) | GET | Retrieves map element groups from Felt. |

### Map Layer

| Action | Method | Description |
| --- | --- | --- |
| [Update Map Layer](actions/update-map-layer.md) | PUT | Updates an existing map layer in Felt. |

### Map Layer Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Map Layer Group](actions/get-map-layer-group.md) | GET | Retrieves a map layer group from Felt. |
| [List Map Layer Groups](actions/list-map-layer-groups.md) | GET | Retrieves map layer groups from Felt. |
| [Update Map Layer Group](actions/update-map-layer-group.md) | PUT | Updates an existing map layer group in Felt. |

### Map Layer Style

| Action | Method | Description |
| --- | --- | --- |
| [Update Layer Style](actions/update-layer-style.md) | PUT | Updates a map layer style in Felt. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Felt. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Felt. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Felt. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Felt. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Felt. |

### Published Layer

| Action | Method | Description |
| --- | --- | --- |
| [Publish Map Layer](actions/publish-map-layer.md) | POST | Publishes a map layer to Felt's library. |

### Published Layer Group

| Action | Method | Description |
| --- | --- | --- |
| [Publish Map Layer Group](actions/publish-map-layer-group.md) | POST | Publishes a map layer group to Felt's library. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Source](actions/create-source.md) | POST | Creates a new data source in Felt. |
| [Delete Source](actions/delete-source.md) | DELETE | Deletes an existing data source from Felt. |
| [Get Source](actions/get-source.md) | GET | Retrieves a data source from Felt. |
| [List Sources](actions/list-sources.md) | GET | Retrieves data sources from Felt. |
| [Sync Source](actions/sync-source.md) | PUT | Syncs a data source in Felt. |
| [Update Source](actions/update-source.md) | PUT | Updates an existing data source in Felt. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the authenticated user's profile from Felt. |

