# <img src="https://images.mindcloud.co/apps/icons/pinboard_1774372984469.png" alt="Pinboard logo" width="28" height="28"> Pinboard: Universal API

Save, organize, and search bookmarks and notes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pinboard/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pinboard.in
- **Vendor API docs:** https://pinboard.in/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Latest Bookmark Update](actions/get-latest-bookmark-update.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/get-latest-bookmark-update?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Api Token

| Action | Method | Description |
| --- | --- | --- |
| [Get User API Token](actions/get-user-api-token.md) | GET |  |

### Bookmark

| Action | Method | Description |
| --- | --- | --- |
| [Add Bookmark](actions/add-bookmark.md) | POST |  |
| [Delete Bookmark](actions/delete-bookmark.md) | DELETE |  |
| [List All Posts](actions/list-all-posts.md) | GET |  |
| [List Posts](actions/list-posts.md) | GET |  |
| [List Recent Posts](actions/list-recent-posts.md) | GET |  |

### Bookmark Date

| Action | Method | Description |
| --- | --- | --- |
| [List Post Dates](actions/list-post-dates.md) | GET |  |

### Bookmark Update

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Bookmark Update](actions/get-latest-bookmark-update.md) | GET |  |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Get Note](actions/get-note.md) | GET |  |
| [List Notes](actions/list-notes.md) | GET |  |

### Secret

| Action | Method | Description |
| --- | --- | --- |
| [Get User Secret](actions/get-user-secret.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Delete Tag](actions/delete-tag.md) | DELETE |  |
| [List Tags](actions/list-tags.md) | GET |  |

### Tag Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Suggest Tags For URL](actions/suggest-tags-for-url.md) | GET |  |

