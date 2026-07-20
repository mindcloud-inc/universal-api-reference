# Toodledo: Native API Reference

A consolidated summary of Toodledo's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.toodledo.com/3/
- **API base URL:** `https://api.toodledo.com/3`

## Authentication

### OAuth2

Connect your Toodledo account with OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.toodledo.com/3/account/authorize.php to approve access.
2. Exchange the returned authorization code with a POST request to https://api.toodledo.com/3/account/token.php.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `basic tasks notes outlines lists folders share write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.toodledo.com/3/account/token.php.

[Official authentication documentation](https://api.toodledo.com/3/account/index.php)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Lists](actions/create-lists.md) | `POST /lists/add.php` | [docs](https://api.toodledo.com/3/lists/index.php) |
| [Create Notes](actions/create-notes.md) | `POST /notes/add.php` | [docs](https://api.toodledo.com/3/notes/index.php) |
| [Create Outlines](actions/create-outlines.md) | `POST /outlines/add.php` | [docs](https://api.toodledo.com/3/outlines/index.php) |
| [Create Rows](actions/create-rows.md) | `POST /rows/add.php` | [docs](https://api.toodledo.com/3/rows/index.php) |
| [Create Tasks](actions/create-tasks.md) | `POST /tasks/add.php` | [docs](https://api.toodledo.com/3/tasks/index.php) |
| [Delete Lists](actions/delete-lists.md) | `POST /lists/delete.php` | [docs](https://api.toodledo.com/3/lists/index.php) |
| [Delete Notes](actions/delete-notes.md) | `POST /notes/delete.php` | [docs](https://api.toodledo.com/3/notes/index.php) |
| [Delete Outlines](actions/delete-outlines.md) | `POST /outlines/delete.php` | [docs](https://api.toodledo.com/3/outlines/index.php) |
| [Delete Rows](actions/delete-rows.md) | `POST /rows/delete.php` | [docs](https://api.toodledo.com/3/rows/index.php) |
| [Delete Tasks](actions/delete-tasks.md) | `POST /tasks/delete.php` | [docs](https://api.toodledo.com/3/tasks/index.php) |
| [Get Account Info](actions/get-account-info.md) | `GET /account/get.php` | [docs](https://api.toodledo.com/3/account/doc_info.php) |
| [List Collaborators](actions/list-collaborators.md) | `GET /account/collaborators.php` | [docs](https://api.toodledo.com/3/tasks/doc_collab.php) |
| [List Deleted Lists](actions/list-deleted-lists.md) | `GET /lists/deleted.php` | [docs](https://api.toodledo.com/3/lists/index.php) |
| [List Deleted Notes](actions/list-deleted-notes.md) | `GET /notes/deleted.php` | [docs](https://api.toodledo.com/3/notes/index.php) |
| [List Deleted Outlines](actions/list-deleted-outlines.md) | `GET /outlines/deleted.php` | [docs](https://api.toodledo.com/3/outlines/index.php) |
| [List Deleted Rows](actions/list-deleted-rows.md) | `GET /rows/deleted.php` | [docs](https://api.toodledo.com/3/rows/index.php) |
| [List Deleted Tasks](actions/list-deleted-tasks.md) | `GET /tasks/deleted.php` | [docs](https://api.toodledo.com/3/tasks/index.php) |
| [List Lists](actions/list-lists.md) | `GET /lists/get.php` | [docs](https://api.toodledo.com/3/lists/index.php) |
| [List Notes](actions/list-notes.md) | `GET /notes/get.php` | [docs](https://api.toodledo.com/3/notes/index.php) |
| [List Outlines](actions/list-outlines.md) | `GET /outlines/get.php` | [docs](https://api.toodledo.com/3/outlines/index.php) |
| [List Rows](actions/list-rows.md) | `GET /rows/get.php` | [docs](https://api.toodledo.com/3/rows/index.php) |
| [List Saved Searches](actions/list-saved-searches.md) | `GET /tasks/search.php` | [docs](https://api.toodledo.com/3/tasks/doc_search.php) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks/get.php` | [docs](https://api.toodledo.com/3/tasks/index.php) |
| [Reassign Task](actions/reassign-task.md) | `POST /tasks/reassign.php` | [docs](https://api.toodledo.com/3/tasks/doc_collab.php) |
| [Share Task](actions/share-task.md) | `POST /tasks/share.php` | [docs](https://api.toodledo.com/3/tasks/doc_collab.php) |
| [Update Lists](actions/update-lists.md) | `POST /lists/edit.php` | [docs](https://api.toodledo.com/3/lists/index.php) |
| [Update Notes](actions/update-notes.md) | `POST /notes/edit.php` | [docs](https://api.toodledo.com/3/notes/index.php) |
| [Update Outlines](actions/update-outlines.md) | `POST /outlines/edit.php` | [docs](https://api.toodledo.com/3/outlines/index.php) |
| [Update Rows](actions/update-rows.md) | `POST /rows/edit.php` | [docs](https://api.toodledo.com/3/rows/index.php) |
| [Update Tasks](actions/update-tasks.md) | `POST /tasks/edit.php` | [docs](https://api.toodledo.com/3/tasks/index.php) |
