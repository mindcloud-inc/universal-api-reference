# <img src="https://images.mindcloud.co/apps/icons/raindrop_1775829026433.png" alt="Raindrop logo" width="28" height="28"> Raindrop: Universal API

Save, organize, search, and share bookmarks, articles, images, and highlights from Raindrop.io.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/raindrop/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://raindrop.io/
- **Vendor API docs:** https://developer.raindrop.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Backup

| Action | Method | Description |
| --- | --- | --- |
| [Generate Backup](actions/generate-backup.md) | GET |  |
| [Get All Backups](actions/get-all-backups.md) | GET |  |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST |  |
| [Delete Collection](actions/delete-collection.md) | DELETE |  |
| [Empty Trash](actions/empty-trash.md) | DELETE |  |
| [Get Child Collections](actions/get-child-collections.md) | GET |  |
| [Get Collection](actions/get-collection.md) | GET |  |
| [Get Root Collections](actions/get-root-collections.md) | GET |  |
| [Get System Collection Counts](actions/get-system-collection-counts.md) | GET |  |
| [Merge Collections](actions/merge-collections.md) | PUT |  |
| [Remove Empty Collections](actions/remove-empty-collections.md) | PUT |  |
| [Remove Multiple Collections](actions/remove-multiple-collections.md) | DELETE |  |
| [Reorder All Collections](actions/reorder-all-collections.md) | PUT |  |
| [Set Collections Expanded State](actions/set-collections-expanded-state.md) | PUT |  |
| [Update Collection](actions/update-collection.md) | PUT |  |

### Collection Cover

| Action | Method | Description |
| --- | --- | --- |
| [Get Featured Collection Covers](actions/get-featured-collection-covers.md) | GET |  |
| [Search Collection Covers](actions/search-collection-covers.md) | GET |  |

### Filter

| Action | Method | Description |
| --- | --- | --- |
| [Get Filters](actions/get-filters.md) | GET |  |

### Highlight

| Action | Method | Description |
| --- | --- | --- |
| [Add Highlight](actions/add-highlight.md) | PUT |  |
| [Get All Highlights](actions/get-all-highlights.md) | GET |  |
| [Get Collection Highlights](actions/get-collection-highlights.md) | GET |  |
| [Remove Highlight](actions/remove-highlight.md) | PUT |  |
| [Update Highlight](actions/update-highlight.md) | PUT |  |

### Parsed Url

| Action | Method | Description |
| --- | --- | --- |
| [Parse URL](actions/parse-url.md) | GET |  |

### Raindrop

| Action | Method | Description |
| --- | --- | --- |
| [Create Raindrop](actions/create-raindrop.md) | POST |  |
| [Get Raindrop](actions/get-raindrop.md) | GET |  |
| [Get Raindrops](actions/get-raindrops.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Tags](actions/get-tags.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET |  |
| [Get Public User](actions/get-public-user.md) | GET |  |

