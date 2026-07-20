# Cirra: Native API Reference

A consolidated summary of Cirra's API configuration and 24 documented operations.

- **API base URL:** `http://api-public:9801`

## Authentication

### Public API Key

Authenticate Cirra thread actions with a MindCloud Public API key. Requests run as the key creator within the key company scope.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.mindcloud.co/docs/create-an-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `offset` in the query string as the record offset.

## Endpoints (24 documented)

| Operation | Method & path |
| --- | --- |
| [Archive Thread](actions/archive-thread.md) | `PUT /v1/cirra/threads/:threadId/archive` |
| [Clear Thread Messages](actions/clear-thread-messages.md) | `DELETE /v1/cirra/threads/:threadId/messages` |
| [Create Role](actions/create-role.md) | `POST /v1/cirra/roles` |
| [Create Thread](actions/create-thread.md) | `POST /v1/cirra/threads` |
| [Delete Connection](actions/delete-connection.md) | `DELETE /v1/cirra/connections/:credentialId` |
| [Delete Role](actions/delete-role.md) | `DELETE /v1/cirra/roles/:roleId` |
| [Get Settings](actions/get-settings.md) | `GET /v1/cirra/settings` |
| [Get User Apps](actions/get-user-apps.md) | `GET /v1/cirra/apps` |
| [Invite Members](actions/invite-members.md) | `POST /v1/members` |
| [List Connections](actions/list-connections.md) | `GET /v1/cirra/connections` |
| [List Members](actions/list-members.md) | `GET /v1/members` |
| [List Role App Permissions](actions/list-role-app-permissions.md) | `GET /v1/cirra/roles/:roleId/permissions/apps` |
| [List Role Model Permissions](actions/list-role-model-permissions.md) | `GET /v1/cirra/roles/:roleId/permissions/apps/:appId/models` |
| [List Roles](actions/list-roles.md) | `GET /v1/cirra/roles` |
| [List Threads](actions/list-threads.md) | `GET /v1/cirra/threads` |
| [Get Thread](actions/read-thread.md) | `GET /v1/cirra/threads/:threadId` |
| [Remove Member](actions/remove-member.md) | `DELETE /v1/members/:userId` |
| [Send Thread Message](actions/send-thread-message.md) | `POST /v1/cirra/threads/:threadId/messages` |
| [Set Global Role Permissions](actions/set-global-role-permissions.md) | `PUT /v1/cirra/roles/:roleId/permissions/global` |
| [Set Member Role](actions/set-member-role.md) | `PUT /v1/members/:userId` |
| [Set Role App Permissions](actions/set-role-app-permissions.md) | `PUT /v1/cirra/roles/:roleId/permissions/apps/:appId` |
| [Set Role Model Permissions](actions/set-role-model-permissions.md) | `PUT /v1/cirra/roles/:roleId/permissions/apps/:appId/models/:modelKey` |
| [Unarchive Thread](actions/unarchive-thread.md) | `DELETE /v1/cirra/threads/:threadId/archive` |
| [Update Settings](actions/update-settings.md) | `PUT /v1/cirra/settings` |
