# SmugMug: Native API Reference

A consolidated summary of SmugMug's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://api.smugmug.com/api/v2/doc
- **API base URL:** `https://api.smugmug.com/api/v2`

## Authentication

### API Key

Use a SmugMug developer API key for public-data access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.smugmug.com/api/v2/doc/tutorial/api-key.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `count` in the query string to set the page size. Use `start` in the query string as the record offset; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Album](actions/get-album.md) | `GET /album/:albumKey` | [docs](https://api.smugmug.com/api/v2/doc/reference/album.html) |
| [Get Album Highlight Image](actions/get-album-highlight-image.md) | `GET /album/:albumKey!highlightimage` | [docs](https://api.smugmug.com/api/v2/doc/reference/album.html) |
| [Get Album Image](actions/get-album-image.md) | `GET /album/:albumKey/image/:imageUriId` | [docs](https://api.smugmug.com/api/v2/doc/reference/album-image.html) |
| [Get Folder](actions/get-folder.md) | `GET /folder/user/:nickname` | [docs](https://api.smugmug.com/api/v2/doc/reference/folder.html) |
| [Get Folder By ID](actions/get-folder-by-id.md) | `GET /folder/id/:folderId` | [docs](https://api.smugmug.com/api/v2/doc/reference/folder.html) |
| [Get Image](actions/get-image.md) | `GET /image/:imageUriId` | [docs](https://api.smugmug.com/api/v2/doc/reference/image.html) |
| [Get Image Metadata](actions/get-image-metadata.md) | `GET /image/:imageUriId!metadata` | [docs](https://api.smugmug.com/api/v2/doc/reference/image.html) |
| [Get Image Size Details](actions/get-image-size-details.md) | `GET /image/:imageUriId!sizedetails` | [docs](https://api.smugmug.com/api/v2/doc/reference/image.html) |
| [Get Node](actions/get-node.md) | `GET /node/:nodeId` | [docs](https://api.smugmug.com/api/v2/doc/reference/node.html) |
| [Get User](actions/get-user.md) | `GET /user/:nickname` | [docs](https://api.smugmug.com/api/v2/doc/reference/user.html) |
| [Get User Profile](actions/get-user-profile.md) | `GET /user/:nickname!profile` | [docs](https://api.smugmug.com/api/v2/doc/reference/user-profile.html) |
| [List Album Images](actions/list-album-images.md) | `GET /album/:albumKey!images` | [docs](https://api.smugmug.com/api/v2/doc/reference/album.html) |
| [List Album Popular Media](actions/list-album-popular-media.md) | `GET /album/:albumKey!popularmedia` | [docs](https://api.smugmug.com/api/v2/doc/reference/album.html) |
| [List Child Nodes](actions/list-child-nodes.md) | `GET /node/:nodeId!children` | [docs](https://api.smugmug.com/api/v2/doc/reference/node.html) |
| [List Folder Albums](actions/list-folder-albums.md) | `GET /folder/user/:nickname!albums` | [docs](https://api.smugmug.com/api/v2/doc/reference/folder.html) |
| [List Folder Folders](actions/list-folder-folders.md) | `GET /folder/user/:nickname!folders` | [docs](https://api.smugmug.com/api/v2/doc/reference/folder.html) |
| [List Parent Nodes](actions/list-parent-nodes.md) | `GET /node/:nodeId!parents` | [docs](https://api.smugmug.com/api/v2/doc/reference/node.html) |
| [List User Albums](actions/list-user-albums.md) | `GET /user/:nickname!albums` | [docs](https://api.smugmug.com/api/v2/doc/reference/user.html) |
| [List User Popular Media](actions/list-user-popular-media.md) | `GET /user/:nickname!popularmedia` | [docs](https://api.smugmug.com/api/v2/doc/reference/user.html) |
| [List User Recent Images](actions/list-user-recent-images.md) | `GET /user/:nickname!recentimages` | [docs](https://api.smugmug.com/api/v2/doc/reference/user.html) |
