# <img src="https://images.mindcloud.co/apps/icons/dashapp_1774538404984.png" alt="Dash.app logo" width="28" height="28"> Dash.app: Universal API

Manage digital assets, metadata, users, collections, and portals

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dashapp/latest
- **Category:** Content & Files / Storage
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dash.app
- **Vendor API docs:** https://api-docs.dash.app/dash/openapi

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Dash.app. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Search Collections](actions/search-collections.md) | GET | Finds collections in Dash.app by search criteria. |

### Corebook Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Corebook Settings](actions/get-corebook-settings.md) | GET | Retrieves Corebook settings from your Dash.app account. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Field](actions/get-field.md) | GET | Retrieves a metadata field from Dash.app by ID. |

### Field Views

| Action | Method | Description |
| --- | --- | --- |
| [Get Field Views](actions/get-field-views.md) | GET | Retrieves field views from your Dash.app account. |

### Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Fields](actions/get-fields.md) | GET | Retrieves metadata fields from your Dash.app account. |

### Folder Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Folder Settings](actions/get-folder-settings.md) | GET | Retrieves folder settings from your Dash.app account. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Dash.app by ID. |

### Grouped Preset Transformations

| Action | Method | Description |
| --- | --- | --- |
| [Get Grouped Preset Transformations](actions/get-grouped-preset-transformations.md) | GET | Retrieves grouped preset transformations from Dash.app. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Groups](actions/get-groups.md) | GET | Retrieves groups from your Dash.app account. |

### Portal

| Action | Method | Description |
| --- | --- | --- |
| [Create Portal](actions/create-portal.md) | POST | Creates a new portal in Dash.app. |
| [Get Portal](actions/get-portal.md) | GET | Retrieves a portal from Dash.app by ID. |

### Portals

| Action | Method | Description |
| --- | --- | --- |
| [Search Portals](actions/search-portals.md) | GET | Finds portals in Dash.app by search criteria. |

### Preset Transformations

| Action | Method | Description |
| --- | --- | --- |
| [Search Preset Transformations](actions/search-preset-transformations.md) | GET | Finds preset transformations in Dash.app by search criteria. |

### Saved Search

| Action | Method | Description |
| --- | --- | --- |
| [Create Saved Search](actions/create-saved-search.md) | POST | Creates a new saved search in Dash.app. |
| [Get Saved Search](actions/get-saved-search.md) | GET | Retrieves a saved search from Dash.app by ID. |

### Saved Searches

| Action | Method | Description |
| --- | --- | --- |
| [Search Saved Searches](actions/search-saved-searches.md) | GET | Finds saved searches in Dash.app by search criteria. |

### Search Filter View

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Filter View](actions/get-search-filter-view.md) | GET | Retrieves the search filter view from Dash.app. |

### Themes

| Action | Method | Description |
| --- | --- | --- |
| [Search Themes](actions/search-themes.md) | GET | Finds themes in Dash.app by search criteria. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Asset Share](actions/create-asset-share.md) | POST | Creates a new asset share in Dash.app. |
| [Delete Asset Share](actions/delete-asset-share.md) | DELETE | Deletes an existing asset share from Dash.app. |
| [Get Asset](actions/get-asset.md) | GET | Retrieves an asset from Dash.app by ID. |
| [Get Asset Files](actions/get-asset-files.md) | GET | Retrieves files for an asset from Dash.app. |
| [Get Asset Share](actions/get-asset-share.md) | GET | Retrieves an asset share from Dash.app by ID. |
| [Get Field Option](actions/get-field-option.md) | GET | Retrieves a field option from Dash.app by ID. |
| [Search Asset Download Events](actions/search-asset-download-events.md) | GET | Finds asset download events in Dash.app by search criteria. |
| [Search Assets](actions/search-assets.md) | GET | Finds assets in Dash.app by search criteria. |
| [Search Field Options](actions/search-field-options.md) | GET | Finds field options in Dash.app by search criteria. |
| [Update Asset Share](actions/update-asset-share.md) | PUT | Updates an existing asset share in Dash.app. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Dash.app. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Dash.app by ID. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Search Users](actions/search-users.md) | GET | Finds users in Dash.app by search criteria. |

