# Frame.io v4: Native API Reference

A consolidated summary of Frame.io v4's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://next.developer.frame.io/platform/api-reference
- **OpenAPI specification:** https://api.frame.io/v4/openapi.json
- **API base URL:** `https://api.frame.io/v4`

## Authentication

### OAuth 2.0

Adobe IMS OAuth user authentication for Frame.io v4

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://ims-na1.adobelogin.com/ims/authorize/v2 to approve access.
2. Exchange the returned authorization code with a POST request to https://ims-na1.adobelogin.com/ims/token/v3.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid profile offline_access additional_info.roles`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://ims-na1.adobelogin.com/ims/token/v3.

[Official authentication documentation](https://next.developer.frame.io/platform/docs/guides/authentication/overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `links.next`.

## Pagination

Use `page_size` in the query string to set the page size. Use `after` in the query string as the pagination cursor.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy File](actions/copy-file.md) | `POST /accounts/:accountId/files/:fileId/copy` | [docs](https://next.developer.frame.io/platform/api-reference/files/copy) |
| [Copy Folder](actions/copy-folder.md) | `POST /accounts/:accountId/folders/:folderId/copy` | [docs](https://next.developer.frame.io/platform/api-reference/folders/copy) |
| [Copy Version Stack](actions/copy-version-stack.md) | `POST /accounts/:accountId/version_stacks/:versionStackId/copy` | [docs](https://next.developer.frame.io/platform/api-reference/version-stacks/copy) |
| [Create Comment](actions/create-comment.md) | `POST /accounts/:accountId/files/:fileId/comments` | [docs](https://next.developer.frame.io/platform/api-reference/comments/create) |
| [Create File Local Upload](actions/create-file-local-upload.md) | `POST /accounts/:accountId/folders/:folderId/files/local_upload` | [docs](https://next.developer.frame.io/platform/api-reference/files/create-local-upload) |
| [Create File Remote Upload](actions/create-file-remote-upload.md) | `POST /accounts/:accountId/folders/:folderId/files/remote_upload` | [docs](https://next.developer.frame.io/platform/api-reference/files/create-remote-upload) |
| [Create Folder](actions/create-folder.md) | `POST /accounts/:accountId/folders/:folderId/folders` | [docs](https://next.developer.frame.io/platform/api-reference/folders/create) |
| [Create Project](actions/create-project.md) | `POST /accounts/:accountId/workspaces/:workspaceId/projects` | [docs](https://next.developer.frame.io/platform/api-reference/projects/create) |
| [Create Share](actions/create-share.md) | `POST /accounts/:accountId/projects/:projectId/shares` | [docs](https://next.developer.frame.io/platform/api-reference/shares/create) |
| [Create Version Stack](actions/create-version-stack.md) | `POST /accounts/:accountId/folders/:folderId/version_stacks` | [docs](https://next.developer.frame.io/platform/api-reference/version-stacks/create) |
| [Create Workspace](actions/create-workspace.md) | `POST /accounts/:accountId/workspaces` | [docs](https://next.developer.frame.io/platform/api-reference/workspaces/create) |
| [Get Comment](actions/get-comment.md) | `GET /accounts/:accountId/comments/:commentId` | [docs](https://next.developer.frame.io/platform/api-reference/comments/show) |
| [Get File](actions/get-file.md) | `GET /accounts/:accountId/files/:fileId` | [docs](https://next.developer.frame.io/platform/api-reference/files/show) |
| [Get File Upload Status](actions/get-file-upload-status.md) | `GET /accounts/:accountId/files/:fileId/status` | [docs](https://next.developer.frame.io/platform/api-reference/files/show-file-upload-status) |
| [Get Folder](actions/get-folder.md) | `GET /accounts/:accountId/folders/:folderId` | [docs](https://next.developer.frame.io/platform/api-reference/folders/show) |
| [Get Project](actions/get-project.md) | `GET /accounts/:accountId/projects/:projectId` | [docs](https://next.developer.frame.io/platform/api-reference/projects/show) |
| [Get Share](actions/get-share.md) | `GET /accounts/:accountId/shares/:shareId` | [docs](https://next.developer.frame.io/platform/api-reference/shares/show) |
| [Get User Details](actions/get-user-details.md) | `GET /me` | [docs](https://next.developer.frame.io/platform/api-reference/users/show) |
| [Get Version Stack](actions/get-version-stack.md) | `GET /accounts/:accountId/version_stacks/:versionStackId` | [docs](https://next.developer.frame.io/platform/api-reference/version-stacks/show) |
| [Get Workspace](actions/get-workspace.md) | `GET /accounts/:accountId/workspaces/:workspaceId` | [docs](https://next.developer.frame.io/platform/api-reference/workspaces/show) |
| [Import File](actions/import-file.md) | `POST /accounts/:accountId/folders/:folderId/files/import` | [docs](https://next.developer.frame.io/platform/api-reference/files/import-file) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://next.developer.frame.io/platform/api-reference/accounts/index) |
| [List Comments](actions/list-comments.md) | `GET /accounts/:accountId/files/:fileId/comments` | [docs](https://next.developer.frame.io/platform/api-reference/comments/index) |
| [List Files](actions/list-files.md) | `GET /accounts/:accountId/folders/:folderId/files` | [docs](https://next.developer.frame.io/platform/api-reference/files/list) |
| [List Folder Children](actions/list-folder-children.md) | `GET /accounts/:accountId/folders/:folderId/children` | [docs](https://next.developer.frame.io/platform/api-reference/folders/index) |
| [List Folders](actions/list-folders.md) | `GET /accounts/:accountId/folders/:folderId/folders` | [docs](https://next.developer.frame.io/platform/api-reference/folders/list) |
| [List Projects](actions/list-projects.md) | `GET /accounts/:accountId/workspaces/:workspaceId/projects` | [docs](https://next.developer.frame.io/platform/api-reference/projects/index) |
| [List Shares](actions/list-shares.md) | `GET /accounts/:accountId/projects/:projectId/shares` | [docs](https://next.developer.frame.io/platform/api-reference/shares/index) |
| [List Version Stack Children](actions/list-version-stack-children.md) | `GET /accounts/:accountId/version_stacks/:versionStackId/children` | [docs](https://next.developer.frame.io/platform/api-reference/version-stacks/index) |
| [List Version Stacks](actions/list-version-stacks.md) | `GET /accounts/:accountId/folders/:folderId/version_stacks` | [docs](https://next.developer.frame.io/platform/api-reference/version-stacks/list) |
| [List Workspaces](actions/list-workspaces.md) | `GET /accounts/:accountId/workspaces` | [docs](https://next.developer.frame.io/platform/api-reference/workspaces/index) |
| [Move File](actions/move-file.md) | `PATCH /accounts/:accountId/files/:fileId/move` | [docs](https://next.developer.frame.io/platform/api-reference/files/move) |
| [Move Folder](actions/move-folder.md) | `PATCH /accounts/:accountId/folders/:folderId/move` | [docs](https://next.developer.frame.io/platform/api-reference/folders/move) |
| [Move Version Stack](actions/move-version-stack.md) | `PATCH /accounts/:accountId/version_stacks/:versionStackId/move` | [docs](https://next.developer.frame.io/platform/api-reference/version-stacks/move) |
| [Update Comment](actions/update-comment.md) | `PATCH /accounts/:accountId/comments/:commentId` | [docs](https://next.developer.frame.io/platform/api-reference/comments/update) |
| [Update File](actions/update-file.md) | `PATCH /accounts/:accountId/files/:fileId` | [docs](https://next.developer.frame.io/platform/api-reference/files/update) |
| [Update Folder](actions/update-folder.md) | `PATCH /accounts/:accountId/folders/:folderId` | [docs](https://next.developer.frame.io/platform/api-reference/folders/update) |
| [Update Project](actions/update-project.md) | `PATCH /accounts/:accountId/projects/:projectId` | [docs](https://next.developer.frame.io/platform/api-reference/projects/update) |
| [Update Share](actions/update-share.md) | `PATCH /accounts/:accountId/shares/:shareId` | [docs](https://next.developer.frame.io/platform/api-reference/shares/update) |
| [Update Workspace](actions/update-workspace.md) | `PATCH /accounts/:accountId/workspaces/:workspaceId` | [docs](https://next.developer.frame.io/platform/api-reference/workspaces/update) |
