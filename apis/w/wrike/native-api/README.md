# Wrike: Native API Reference

A consolidated summary of Wrike's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.wrike.com/overview/
- **API base URL:** `https://{host}/api/v4`

## Authentication

### OAuth2

OAuth 2.0 authorization for Wrike.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.wrike.com/oauth2/authorize/v4 to approve access.
2. Exchange the returned authorization code with a POST request to https://login.wrike.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `Default,wsReadOnly,wsReadWrite,amReadOnlyWorkflow,amReadWriteWorkflow,amReadOnlyInvitation,amReadWriteInvitation,amReadOnlyGroup,amReadWriteGroup,amReadOnlyUser,amReadWriteUser`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.wrike.com/oauth2/token.

[Official authentication documentation](https://developers.wrike.com/oauth-20-authorization/)

## API conventions

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | `POST /folders/:folderId/folders` | [docs](https://developers.wrike.com/api/v4/folders-projects/) |
| [Create Task](actions/create-task.md) | `POST /folders/:folderId/tasks` | [docs](https://developers.wrike.com/api/v4/tasks/) |
| [Create Task Comment](actions/create-task-comment.md) | `POST /tasks/:taskId/comments` | [docs](https://developers.wrike.com/api/v4/comments/) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /folders/:folderId` | [docs](https://developers.wrike.com/api/v4/folders-projects/) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:taskId` | [docs](https://developers.wrike.com/api/v4/tasks/) |
| [Get Access URL for Attachment](actions/get-access-url-for-attachment.md) | `GET /attachments/:attachmentId/url` | [docs](https://developers.wrike.com/api/v4/attachments/) |
| [Get Space](actions/get-space.md) | `GET /spaces/:spaceId` | [docs](https://developers.wrike.com/api/v4/spaces/) |
| [List Attachments](actions/list-attachments.md) | `GET /attachments` | [docs](https://developers.wrike.com/api/v4/attachments/) |
| [List Comments](actions/list-comments.md) | `GET /comments` | [docs](https://developers.wrike.com/api/v4/comments/) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.wrike.com/api/v4/contacts/) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /customfields` | [docs](https://developers.wrike.com/api/v4/custom-fields/) |
| [List Folder Children](actions/list-folder-children.md) | `GET /folders/:folderId/folders` | [docs](https://developers.wrike.com/api/v4/folders-projects/) |
| [List Folder Tasks](actions/list-folder-tasks.md) | `GET /folders/:folderId/tasks` | [docs](https://developers.wrike.com/api/v4/tasks/) |
| [List Folders](actions/list-folders.md) | `GET /folders` | [docs](https://developers.wrike.com/api/v4/folders-projects/) |
| [List Space Folders](actions/list-space-folders.md) | `GET /spaces/:spaceId/folders` | [docs](https://developers.wrike.com/api/v4/folders-projects/) |
| [List Space Tasks](actions/list-space-tasks.md) | `GET /spaces/:spaceId/tasks` | [docs](https://developers.wrike.com/api/v4/tasks/) |
| [List Spaces](actions/list-spaces.md) | `GET /spaces` | [docs](https://developers.wrike.com/api/v4/spaces/) |
| [List Task Attachments](actions/list-task-attachments.md) | `GET /tasks/:taskId/attachments` | [docs](https://developers.wrike.com/api/v4/attachments/) |
| [List Task Comments](actions/list-task-comments.md) | `GET /tasks/:taskId/comments` | [docs](https://developers.wrike.com/api/v4/comments/) |
| [List Task Dependencies](actions/list-task-dependencies.md) | `GET /tasks/:taskId/dependencies` | [docs](https://developers.wrike.com/api/v4/dependencies/) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://developers.wrike.com/api/v4/tasks/) |
| [Update Comment](actions/update-comment.md) | `PUT /comments/:commentId` | [docs](https://developers.wrike.com/api/v4/comments/) |
| [Update Folder](actions/update-folder.md) | `PUT /folders/:folderId` | [docs](https://developers.wrike.com/api/v4/folders-projects/) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:taskId` | [docs](https://developers.wrike.com/api/v4/tasks/) |
