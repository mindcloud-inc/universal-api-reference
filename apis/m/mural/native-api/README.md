# Mural: Native API Reference

A consolidated summary of Mural's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.mural.co/public/reference/intro
- **OpenAPI specification:** https://developers.mural.co/public/openapi/60959cbc7ff8b600451a3da6
- **API base URL:** `https://app.mural.co/api/public/v1`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.mural.co/api/public/v1/authorization/oauth2/ to approve access.
2. Exchange the returned authorization code with a POST request to https://app.mural.co/api/public/v1/authorization/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `rooms:read users:read workspaces:read murals:read identity:read templates:read`.

PKCE is enabled. The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://app.mural.co/api/public/v1/authorization/oauth2/token.

[Official authentication documentation](https://developers.mural.co/public/docs/oauth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `value`. The next-page cursor is read from `next`.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `next` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Folder in Room](actions/create-folder-in-room.md) | `POST /rooms/:roomId/folders` | [docs](https://developers.mural.co/public/reference/createroomfolder) |
| [Create Mural](actions/create-mural.md) | `POST /murals` | [docs](https://developers.mural.co/public/reference/createmural) |
| [Create Mural from Template](actions/create-mural-from-template.md) | `POST /templates/:templateId/murals` | [docs](https://developers.mural.co/public/reference/createmuralfromtemplate) |
| [Create Room](actions/create-room.md) | `POST /rooms` | [docs](https://developers.mural.co/public/reference/createroom) |
| [Duplicate Mural](actions/duplicate-mural.md) | `POST /murals/:muralId/duplicate` | [docs](https://developers.mural.co/public/reference/duplicatemural) |
| [Export Mural to File](actions/export-mural-to-file.md) | `POST /murals/:muralId/export` | [docs](https://developers.mural.co/public/reference/exportmural) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://developers.mural.co/public/reference/getcurrentmember) |
| [Get Export URL](actions/get-export-url.md) | `GET /murals/:muralId/exports/:exportId` | [docs](https://developers.mural.co/public/reference/exporturlmural) |
| [Get Mural](actions/get-mural.md) | `GET /murals/:muralId` | [docs](https://developers.mural.co/public/reference/getmuralbyid) |
| [Get Room](actions/get-room.md) | `GET /rooms/:roomId` | [docs](https://developers.mural.co/public/reference/getroominfobyid) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/:workspaceId` | [docs](https://developers.mural.co/public/reference/getworkspace) |
| [List Default and Custom Templates for Workspace](actions/list-default-and-custom-templates-for-workspace.md) | `GET /workspaces/:workspaceId/templates` | [docs](https://developers.mural.co/public/reference/gettemplatesbyworkspace) |
| [List Folders for Room](actions/list-folders-for-room.md) | `GET /rooms/:roomId/folders` | [docs](https://developers.mural.co/public/reference/getroomfolders) |
| [List Murals for Room](actions/list-murals-for-room.md) | `GET /rooms/:roomId/murals` | [docs](https://developers.mural.co/public/reference/getroommurals) |
| [List Murals for Workspace](actions/list-murals-for-workspace.md) | `GET /workspaces/:workspaceId/murals` | [docs](https://developers.mural.co/public/reference/getworkspacemurals) |
| [List Open Rooms for Workspace](actions/list-open-rooms-for-workspace.md) | `GET /workspaces/:workspaceId/rooms/open` | [docs](https://developers.mural.co/public/reference/getworkspaceopenrooms) |
| [List Recent Templates for Workspace](actions/list-recent-templates-for-workspace.md) | `GET /workspaces/:workspaceId/templates/recent` | [docs](https://developers.mural.co/public/reference/getrecenttemplates) |
| [List Recently Opened Murals for Workspace](actions/list-recently-opened-murals-for-workspace.md) | `GET /workspaces/:workspaceId/murals/recent` | [docs](https://developers.mural.co/public/reference/getworkspacerecentmurals) |
| [List Rooms for Workspace](actions/list-rooms-for-workspace.md) | `GET /workspaces/:workspaceId/rooms` | [docs](https://developers.mural.co/public/reference/getworkspacerooms) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://developers.mural.co/public/reference/getworkspaces) |
| [Search Murals](actions/search-murals.md) | `GET /search/:workspaceId/murals` | [docs](https://developers.mural.co/public/reference/searchmurals) |
| [Search Rooms](actions/search-rooms.md) | `GET /search/:workspaceId/rooms` | [docs](https://developers.mural.co/public/reference/searchrooms) |
| [Update Mural](actions/update-mural.md) | `PATCH /murals/:muralId` | [docs](https://developers.mural.co/public/reference/updatemuralbyid) |
| [Update Room](actions/update-room.md) | `PATCH /rooms/:roomId` | [docs](https://developers.mural.co/public/reference/updateroombyid) |
