# Samply: Native API Reference

A consolidated summary of Samply's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://docs.samply.app/api/introduction.html
- **API base URL:** `https://samply.app/api/v0`

## Authentication

### API Key

Authenticate Samply API requests with a personal access token using the Authorization Bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.samply.app/api/authentication.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Items To Folder](actions/add-items-to-folder.md) | `POST /projects/:projectid/files/:fileid` | [docs](https://docs.samply.app/api/files.html) |
| [Add Items To Stack](actions/add-items-to-stack.md) | `POST /projects/:projectid/files/:fileid` | [docs](https://docs.samply.app/api/files.html) |
| [Create Comment](actions/create-comment.md) | `POST /projects/:projectid/files/:fileid/comments` | [docs](https://docs.samply.app/api/comments.html) |
| [Create Folder](actions/create-folder.md) | `POST /projects/:projectid/folders` | [docs](https://docs.samply.app/api/files.html) |
| [Create Player](actions/create-player.md) | `POST /players` | [docs](https://docs.samply.app/api/players.html) |
| [Create Private Player](actions/create-private-player.md) | `POST /players` | [docs](https://docs.samply.app/api/players.html) |
| [Create Public Player](actions/create-public-player.md) | `POST /players` | [docs](https://docs.samply.app/api/players.html) |
| [Create Stack](actions/create-stack.md) | `POST /projects/:projectid/stacks` | [docs](https://docs.samply.app/api/files.html) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.samply.app/api/webhooks.html) |
| [Delete File](actions/delete-file.md) | `DELETE /projects/:projectid/files/:fileid` | [docs](https://docs.samply.app/api/files.html) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhookid` | [docs](https://docs.samply.app/api/webhooks.html) |
| [Disable Player Downloads (Tenant-Limited)](actions/disable-player-downloads.md) | `POST /players/:playerid` | [docs](https://docs.samply.app/api/players.html) |
| [Enable Player Downloads](actions/enable-player-downloads.md) | `POST /players/:playerid` | [docs](https://docs.samply.app/api/players.html) |
| [Get File](actions/get-file.md) | `GET /projects/:projectid/files/:fileid` | [docs](https://docs.samply.app/api/files.html) |
| [Get File Download URL](actions/get-file-download-url.md) | `GET /projects/:projectid/files/:fileid/download` | [docs](https://docs.samply.app/api/files.html) |
| [Get Player](actions/get-player.md) | `GET /players/:playerid` | [docs](https://docs.samply.app/api/players.html) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectid` | [docs](https://docs.samply.app/api/projects.html) |
| [List Comments](actions/list-comments.md) | `GET /projects/:projectid/files/:fileid/comments` | [docs](https://docs.samply.app/api/comments.html) |
| [List Folders](actions/list-folders.md) | `GET /projects/:projectid/folders` | [docs](https://docs.samply.app/api/files.html) |
| [List Players](actions/list-players.md) | `GET /players` | [docs](https://docs.samply.app/api/players.html) |
| [List Project Items](actions/list-project-items.md) | `GET /projects/:projectid/all` | [docs](https://docs.samply.app/api/files.html) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.samply.app/api/projects.html) |
| [Publish Player](actions/publish-player.md) | `POST /players/:playerid` | [docs](https://docs.samply.app/api/players.html) |
| [Remove Items From Folder](actions/remove-items-from-folder.md) | `POST /projects/:projectid/files/:fileid` | [docs](https://docs.samply.app/api/files.html) |
| [Remove Items From Stack](actions/remove-items-from-stack.md) | `POST /projects/:projectid/files/:fileid` | [docs](https://docs.samply.app/api/files.html) |
| [Rename File](actions/rename-file.md) | `POST /projects/:projectid/files/:fileid` | [docs](https://docs.samply.app/api/files.html) |
| [Rename Folder](actions/rename-folder.md) | `POST /projects/:projectid/files/:fileid` | [docs](https://docs.samply.app/api/files.html) |
| [Rename Player](actions/rename-player.md) | `POST /players/:playerid` | [docs](https://docs.samply.app/api/players.html) |
| [Rename Project](actions/rename-project.md) | `POST /projects/:projectid` | [docs](https://docs.samply.app/api/projects.html) |
| [Rename Stack](actions/rename-stack.md) | `POST /projects/:projectid/files/:fileid` | [docs](https://docs.samply.app/api/files.html) |
| [Request File Upload](actions/request-file-upload.md) | `POST /projects/:projectid/files` | [docs](https://docs.samply.app/api/files.html) |
| [Unpublish Player](actions/unpublish-player.md) | `POST /players/:playerid` | [docs](https://docs.samply.app/api/players.html) |
| [Update Player](actions/update-player.md) | `POST /players/:playerid` | [docs](https://docs.samply.app/api/players.html) |
| [Update Project](actions/update-project.md) | `POST /projects/:projectid` | [docs](https://docs.samply.app/api/projects.html) |
