# <img src="https://images.mindcloud.co/apps/icons/samply_1774875474417.png" alt="Samply logo" width="28" height="28"> Samply: Universal API

Share audio projects, players, files, comments, and webhooks in Samply.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/samply/latest
- **Category:** Content & Files / Storage
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://samply.app
- **Vendor API docs:** https://docs.samply.app/api/introduction.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samply/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST |  |
| [List Comments](actions/list-comments.md) | GET |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE |  |
| [Get File](actions/get-file.md) | GET |  |
| [Rename File](actions/rename-file.md) | PUT |  |

### File Download

| Action | Method | Description |
| --- | --- | --- |
| [Get File Download URL](actions/get-file-download-url.md) | GET |  |

### File Upload Request

| Action | Method | Description |
| --- | --- | --- |
| [Request File Upload](actions/request-file-upload.md) | POST |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Add Items To Folder](actions/add-items-to-folder.md) | PUT |  |
| [Create Folder](actions/create-folder.md) | POST |  |
| [List Folders](actions/list-folders.md) | GET |  |
| [Remove Items From Folder](actions/remove-items-from-folder.md) | PUT |  |
| [Rename Folder](actions/rename-folder.md) | PUT |  |

### Player

| Action | Method | Description |
| --- | --- | --- |
| [Create Player](actions/create-player.md) | POST |  |
| [Create Private Player](actions/create-private-player.md) | POST |  |
| [Create Public Player](actions/create-public-player.md) | POST |  |
| [Disable Player Downloads (Tenant-Limited)](actions/disable-player-downloads.md) | PUT |  |
| [Enable Player Downloads](actions/enable-player-downloads.md) | PUT |  |
| [Get Player](actions/get-player.md) | GET |  |
| [List Players](actions/list-players.md) | GET |  |
| [Publish Player](actions/publish-player.md) | PUT |  |
| [Rename Player](actions/rename-player.md) | PUT |  |
| [Unpublish Player](actions/unpublish-player.md) | PUT |  |
| [Update Player](actions/update-player.md) | PUT |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Rename Project](actions/rename-project.md) | PUT |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Project Item

| Action | Method | Description |
| --- | --- | --- |
| [List Project Items](actions/list-project-items.md) | GET |  |

### Stack

| Action | Method | Description |
| --- | --- | --- |
| [Add Items To Stack](actions/add-items-to-stack.md) | PUT |  |
| [Create Stack](actions/create-stack.md) | POST |  |
| [Remove Items From Stack](actions/remove-items-from-stack.md) | PUT |  |
| [Rename Stack](actions/rename-stack.md) | PUT |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |

