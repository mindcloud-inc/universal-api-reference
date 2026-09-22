# <img src="https://images.mindcloud.co/apps/icons/box-api-logo_1784316303050.jpeg" alt="Box logo" width="28" height="28"> Box: Universal API

Connect Box to search content, inspect the authenticated user, and work with files and folders through the Box API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/box/latest
- **Category:** Content & Files / Storage
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.box.com/
- **Vendor API docs:** https://developer.box.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/box/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Commit Upload Session](actions/commit-upload-session.md) | POST |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Get Folder](actions/get-folder.md) | GET |  |
| [Search Folders](actions/search-folders.md) | GET |  |

### Folder Item

| Action | Method | Description |
| --- | --- | --- |
| [List Root Folder Items](actions/list-root-folder-items.md) | GET |  |

### Upload Part

| Action | Method | Description |
| --- | --- | --- |
| [Upload Part](actions/upload-part.md) | PUT |  |

### Upload Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Upload Session](actions/create-upload-session.md) | POST |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

