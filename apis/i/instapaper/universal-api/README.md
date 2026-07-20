# <img src="https://images.mindcloud.co/apps/icons/instapaper_1774549349192.png" alt="Instapaper logo" width="28" height="28"> Instapaper: Universal API

Save, organize, and read articles with Instapaper

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/instapaper/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.instapaper.com/
- **Vendor API docs:** https://www.instapaper.com/developers/v1/full-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Credentials](actions/verify-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instapaper/latest/actions/verify-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Add Bookmark](actions/add-bookmark.md) | POST |  |
| [Archive Bookmark](actions/archive-bookmark.md) | PUT |  |
| [Delete Bookmark](actions/delete-bookmark.md) | DELETE |  |
| [Get Bookmark Text](actions/get-bookmark-text.md) | GET |  |
| [List Bookmarks](actions/list-bookmarks.md) | GET |  |
| [Move Bookmark](actions/move-bookmark.md) | PUT |  |
| [Star Bookmark](actions/star-bookmark.md) | PUT |  |
| [Unarchive Bookmark](actions/unarchive-bookmark.md) | PUT |  |
| [Unstar Bookmark](actions/unstar-bookmark.md) | PUT |  |
| [Update Bookmark Read Progress](actions/update-bookmark-read-progress.md) | PUT |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Delete Folder](actions/delete-folder.md) | DELETE |  |
| [List Folders](actions/list-folders.md) | GET |  |
| [Reorder Folders](actions/reorder-folders.md) | PUT |  |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Bookmark Highlight](actions/create-bookmark-highlight.md) | POST |  |
| [Delete Highlight](actions/delete-highlight.md) | DELETE |  |
| [List Bookmark Highlights](actions/list-bookmark-highlights.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Verify Credentials](actions/verify-credentials.md) | GET |  |

