# KleverKey: Native API Reference

A consolidated summary of KleverKey's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://portal.kleverkey.com/documentation/api
- **OpenAPI specification:** https://portal.kleverkey.com/documentation/api/v1/openapi.json
- **API base URL:** `https://api.kleverkey.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://portal.kleverkey.com/documentation/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `PageSize` in the query string to set the page size (default 100; maximum 100000). Use `Page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Access Group](actions/add-access-group.md) | `POST /api/v1/organizations/:organizationId/access-groups` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Add Managed User](actions/add-managed-user.md) | `POST /api/v1/organizations/:organizationId/users/managed` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Add Webhook](actions/add-webhook.md) | `POST /api/v1/organizations/:organizationId/webhooks` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Create Organization](actions/create-organization.md) | `POST /api/v1/organizations` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Delete Managed User](actions/delete-managed-user.md) | `DELETE /api/v1/organizations/:organizationId/users/managed/:userId` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Get Access Group](actions/get-access-group.md) | `GET /api/v1/organizations/:organizationId/access-groups/:accessGroupId` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Get Current User](actions/get-current-user.md) | `GET /api/v1/users/me` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Get Invitation](actions/get-invitation.md) | `GET /api/v1/organizations/:organizationId/invitations/:id` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Get Lock](actions/get-lock.md) | `GET /api/v1/organizations/:organizationId/locks/:lockId` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Get Organization](actions/get-organization.md) | `GET /api/v1/organizations/:organizationId` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Get User](actions/get-user.md) | `GET /api/v1/organizations/:organizationId/users/:userId` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Grant Permission](actions/grant-permission.md) | `PUT /api/v1/organizations/:organizationId/permissions/:lockId/:userId` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Invite User](actions/invite-user.md) | `POST /api/v1/organizations/:organizationId/invitations/user-invitation` | [docs](https://portal.kleverkey.com/documentation/api) |
| [List Access Groups](actions/list-access-groups.md) | `GET /api/v1/organizations/:organizationId/access-groups` | [docs](https://portal.kleverkey.com/documentation/api) |
| [List Invitations](actions/list-invitations.md) | `GET /api/v1/organizations/:organizationId/invitations` | [docs](https://portal.kleverkey.com/documentation/api) |
| [List Locks](actions/list-locks.md) | `GET /api/v1/organizations/:organizationId/locks` | [docs](https://portal.kleverkey.com/documentation/api) |
| [List Permissions](actions/list-permissions.md) | `GET /api/v1/organizations/:organizationId/permissions` | [docs](https://portal.kleverkey.com/documentation/api) |
| [List Users](actions/list-users.md) | `GET /api/v1/organizations/:organizationId/users` | [docs](https://portal.kleverkey.com/documentation/api) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/v1/organizations/:organizationId/webhooks` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Manage Bookings](actions/manage-bookings.md) | `POST /api/v1/organizations/:organizationId/bookings/:serviceName` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Resend Invitation](actions/resend-invitation.md) | `PUT /api/v1/organizations/:organizationId/invitations/:id/resend` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Revoke Permission](actions/revoke-permission.md) | `DELETE /api/v1/organizations/:organizationId/permissions/:lockId/:userId` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Update Access Group Partially](actions/update-access-group-partially.md) | `PATCH /api/v1/organizations/:organizationId/access-groups/:accessGroupId` | [docs](https://portal.kleverkey.com/documentation/api) |
| [Update Managed User](actions/update-managed-user.md) | `PUT /api/v1/organizations/:organizationId/users/managed/:userId` | [docs](https://portal.kleverkey.com/documentation/api) |
