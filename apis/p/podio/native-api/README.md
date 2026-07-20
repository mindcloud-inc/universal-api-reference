# Podio: Native API Reference

A consolidated summary of Podio's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://developers.podio.com/doc
- **API base URL:** `https://api.podio.com`

## Authentication

### OAuth 2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://podio.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.podio.com/oauth/token/v2.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `global:all`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.podio.com/oauth/token/v2.

[Official authentication documentation](https://developers.podio.com/authentication/server_side)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 30). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_desc`. Use `false` for ascending order and `true` for descending order. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Comment to Object](actions/add-comment-to-object.md) | `POST /comment/:type/:id/` | [docs](https://developers.podio.com/doc/comments/add-comment-to-object-22340) |
| [Add Item](actions/add-item.md) | `POST /item/app/:app_id/` | [docs](https://developers.podio.com/doc/items/add-new-item-22362) |
| [Attach File](actions/attach-file.md) | `POST /file/:file_id/attach` | [docs](https://developers.podio.com/doc/files/attach-file-22518) |
| [Complete Task](actions/complete-task.md) | `POST /task/:task_id/complete` | [docs](https://developers.podio.com/doc/tasks/complete-task-22432) |
| [Create Task](actions/create-task.md) | `POST /task/` | [docs](https://developers.podio.com/doc/tasks/create-task-22419) |
| [Delete Item](actions/delete-item.md) | `DELETE /item/:item_id` | [docs](https://developers.podio.com/doc/items/delete-item-22364) |
| [Filter Items](actions/filter-items.md) | `POST /item/app/:app_id/filter/` | [docs](https://developers.podio.com/doc/items/filter-items-4496747) |
| [Filter Items by View](actions/filter-items-by-view.md) | `POST /item/app/:app_id/filter/:view_id/` | [docs](https://developers.podio.com/doc/items/filter-items-by-view-4540284) |
| [Get App](actions/get-app.md) | `GET /app/:app_id` | [docs](https://developers.podio.com/doc/applications/get-app-22349) |
| [Get Item](actions/get-item.md) | `GET /item/:item_id` | [docs](https://developers.podio.com/doc/items/get-item-22360) |
| [Get Item Values v2](actions/get-item-values-v2.md) | `GET /item/:item_id/value/v2` | [docs](https://developers.podio.com/doc/items/get-item-values-v2-144280791) |
| [Get Space](actions/get-space.md) | `GET /space/:space_id` | [docs](https://developers.podio.com/doc/spaces/get-space-22389) |
| [Get Task](actions/get-task.md) | `GET /task/:task_id` | [docs](https://developers.podio.com/doc/tasks/get-task-22413) |
| [Get User Status](actions/get-user-status.md) | `GET /user/status` | [docs](https://developers.podio.com/doc/users/get-user-status-22480) |
| [List Apps](actions/list-apps.md) | `GET /app/` | [docs](https://developers.podio.com/doc/applications/get-all-apps-5902728) |
| [List Apps by Space](actions/list-apps-by-space.md) | `GET /app/space/:space_id/` | [docs](https://developers.podio.com/doc/applications/get-apps-by-space-22478) |
| [List Comments on Object](actions/list-comments-on-object.md) | `GET /comment/:type/:id/` | [docs](https://developers.podio.com/doc/comments/get-comments-on-object-22371) |
| [List Organization Workspaces](actions/list-organization-workspaces.md) | `GET /space/org/:org_id/` | [docs](https://developers.podio.com/doc/spaces/get-list-of-organization-workspaces-238875316) |
| [List Tasks](actions/list-tasks.md) | `GET /task/` | [docs](https://developers.podio.com/doc/tasks/get-tasks-77949) |
| [List Top Spaces](actions/list-top-spaces.md) | `GET /space/top/` | [docs](https://developers.podio.com/doc/spaces/get-top-spaces-22477) |
| [Search in Application v2](actions/search-in-application-v2.md) | `GET /search/app/:app_id/v2` | [docs](https://developers.podio.com/doc/search/search-in-application-v2-155196220) |
| [Search in Space v2](actions/search-in-space-v2.md) | `GET /search/space/:space_id/v2` | [docs](https://developers.podio.com/doc/search/search-in-space-v2-155195763) |
| [Update Item](actions/update-item.md) | `PUT /item/:item_id` | [docs](https://developers.podio.com/doc/items/update-item-22363) |
| [Update Task](actions/update-task.md) | `PUT /task/:task_id` | [docs](https://developers.podio.com/doc/tasks/update-task-10583674) |
| [Upload File](actions/upload-file.md) | `POST /file/` | [docs](https://developers.podio.com/doc/files/upload-file-1004361) |
