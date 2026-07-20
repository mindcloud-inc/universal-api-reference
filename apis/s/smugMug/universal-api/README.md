# <img src="https://images.mindcloud.co/apps/icons/smug-mug_1776799278321.png" alt="SmugMug logo" width="28" height="28"> SmugMug: Universal API

Manage SmugMug photos, albums, folders, and site settings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smugMug/latest
- **Category:** Content & Files / Storage
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smugmug.com
- **Vendor API docs:** https://api.smugmug.com/api/v2/doc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smugMug/latest/actions/get-user?connectionId=$CONNECTION_ID&nickname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Get Album](actions/get-album.md) | GET |  |
| [List Folder Albums](actions/list-folder-albums.md) | GET |  |
| [List User Albums](actions/list-user-albums.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Album Highlight Image](actions/get-album-highlight-image.md) | GET |  |
| [Get Album Image](actions/get-album-image.md) | GET |  |
| [Get Image](actions/get-image.md) | GET |  |
| [Get Image Metadata](actions/get-image-metadata.md) | GET |  |
| [Get Image Size Details](actions/get-image-size-details.md) | GET |  |
| [List Album Images](actions/list-album-images.md) | GET |  |
| [List Album Popular Media](actions/list-album-popular-media.md) | GET |  |
| [List User Popular Media](actions/list-user-popular-media.md) | GET |  |
| [List User Recent Images](actions/list-user-recent-images.md) | GET |  |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Get Folder](actions/get-folder.md) | GET |  |
| [Get Folder By ID](actions/get-folder-by-id.md) | GET |  |
| [List Folder Folders](actions/list-folder-folders.md) | GET |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Node](actions/get-node.md) | GET |  |
| [List Child Nodes](actions/list-child-nodes.md) | GET |  |
| [List Parent Nodes](actions/list-parent-nodes.md) | GET |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |

