# Frontegg: Native API Reference

A consolidated summary of Frontegg's API configuration and 35 documented operations, with links to official documentation.

- **Official docs:** https://developers.frontegg.com/ciam/api/overview
- **OpenAPI specification:** https://raw.githubusercontent.com/frontegg/openapi-public/master/apis-combined.json
- **API base URL:** `https://api.frontegg.com`

## Authentication

### Environment Credentials

Use a Frontegg environment client ID and secret to mint a management token.

### Credentials

- **Client ID:** `clientId` · required · Your Frontegg environment client ID.
- **Secret:** `secret` · required · Your Frontegg environment secret key.

Send these headers with each API request:

```http
Authorization: Bearer <custom.token>
frontegg-tenant-id: <tenantId>
frontegg-user-id: <userId>
```

[Official authentication documentation](https://developers.frontegg.com/ciam/api/vendor-service)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `_limit` in the query string to set the page size (default 50; maximum 200). Use `_offset` in the query string to choose the page; numbering starts at 0.

## Sorting

Set the sort field with `_sortBy` in the query string. Set the direction separately with `_order`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (35 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Roles To Group](actions/add-roles-to-group.md) | `POST /identity/resources/groups/v1/:groupId/roles` | [docs](https://developers.frontegg.com/ciam/api/identity/user-groups) |
| [Add User To Tenant](actions/add-user-to-tenant.md) | `POST /identity/resources/users/v1/:userId/tenant` | [docs](https://developers.frontegg.com/ciam/api/identity/users) |
| [Add Users To Group](actions/add-users-to-group.md) | `POST /identity/resources/groups/v1/:groupId/users` | [docs](https://developers.frontegg.com/ciam/api/identity/user-groups) |
| [Create Account Invite For User](actions/create-account-invite-for-user.md) | `POST /identity/resources/tenants/invites/v1/user` | [docs](https://developers.frontegg.com/ciam/api/identity/account-invitations) |
| [Create Group](actions/create-group.md) | `POST /identity/resources/groups/v1` | [docs](https://developers.frontegg.com/ciam/api/identity/user-groups) |
| [Create Permission](actions/create-permission.md) | `POST /identity/resources/permissions/v1` | [docs](https://developers.frontegg.com/ciam/api/identity/permissions) |
| [Create Role](actions/create-role.md) | `POST /identity/resources/roles/v1` | [docs](https://developers.frontegg.com/ciam/api/identity/roles) |
| [Create Tenant](actions/create-tenant.md) | `POST /tenants/resources/tenants/v1` | [docs](https://developers.frontegg.com/ciam/api/tenants/accounts) |
| [Create User](actions/create-user.md) | `POST /identity/resources/vendor-only/users/v1` | [docs](https://developers.frontegg.com/ciam/api/identity/users) |
| [Delete User](actions/delete-user.md) | `DELETE /identity/resources/users/v1/:userId` | [docs](https://developers.frontegg.com/ciam/api/identity/user-management) |
| [Disable User Account (Tenant)](actions/disable-user-account-tenant.md) | `POST /identity/resources/tenants/users/v1/:userId/disable` | [docs](https://developers.frontegg.com/ciam/api/identity/user-management) |
| [Enable User Account (Tenant)](actions/enable-user-account-tenant.md) | `POST /identity/resources/tenants/users/v1/:userId/enable` | [docs](https://developers.frontegg.com/ciam/api/identity/user-management) |
| [Get Captcha Policy](actions/get-captcha-policy.md) | `GET /identity/resources/configurations/v1/captcha-policy` | [docs](https://developers.frontegg.com/ciam/api/identity/core-settings) |
| [Get Domain Restrictions](actions/get-domain-restrictions.md) | `GET /identity/resources/configurations/restrictions/v1/email-domain` | [docs](https://developers.frontegg.com/ciam/api/identity/domain-restrictions) |
| [Get Environment Token](actions/get-environment-token.md) | `POST /auth/vendor` | [docs](https://developers.frontegg.com/ciam/api/vendor-service) |
| [Get Identity Management Configuration](actions/get-identity-management-configuration.md) | `GET /identity/resources/configurations/v1` | [docs](https://developers.frontegg.com/ciam/api/identity/core-settings) |
| [Get MFA Configuration](actions/get-mfa-configuration.md) | `GET /identity/resources/configurations/v1/mfa` | [docs](https://developers.frontegg.com/ciam/api/identity/mfa-configuration) |
| [Get Tenant](actions/get-tenant.md) | `GET /tenants/resources/tenants/v2/:tenantId` | [docs](https://developers.frontegg.com/ciam/api/tenants/accounts) |
| [Get User](actions/get-user.md) | `GET /identity/resources/users/v1/:id` | [docs](https://developers.frontegg.com/ciam/api/identity/users) |
| [List Groups](actions/list-groups.md) | `GET /identity/resources/groups/v1` | [docs](https://developers.frontegg.com/ciam/api/identity/user-groups) |
| [List Permissions](actions/list-permissions.md) | `GET /identity/resources/permissions/v1` | [docs](https://developers.frontegg.com/ciam/api/identity/permissions) |
| [List Roles](actions/list-roles.md) | `GET /identity/resources/roles/v1` | [docs](https://developers.frontegg.com/ciam/api/identity/roles) |
| [List Tenants](actions/list-tenants.md) | `GET /tenants/resources/tenants/v2` | [docs](https://developers.frontegg.com/ciam/api/tenants/accounts) |
| [List Users](actions/list-users.md) | `GET /identity/resources/users/v3` | [docs](https://developers.frontegg.com/ciam/api/identity/user-management) |
| [Lock User](actions/lock-user.md) | `POST /identity/resources/users/v1/:userId/lock` | [docs](https://developers.frontegg.com/ciam/api/identity/users) |
| [Move Users Between Tenants](actions/move-users-between-tenants.md) | `PUT /identity/resources/users/v1/tenants/migrate` | [docs](https://developers.frontegg.com/ciam/api/identity/users) |
| [Set Permission Roles](actions/set-permission-roles.md) | `PUT /identity/resources/permissions/v1/:permissionId/roles` | [docs](https://developers.frontegg.com/ciam/api/identity/permissions) |
| [Unlock User](actions/unlock-user.md) | `POST /identity/resources/users/v1/:userId/unlock` | [docs](https://developers.frontegg.com/ciam/api/identity/users) |
| [Update Group](actions/update-group.md) | `PATCH /identity/resources/groups/v1/:id` | [docs](https://developers.frontegg.com/ciam/api/identity/user-groups) |
| [Update Identity Management Configuration](actions/update-identity-management-configuration.md) | `POST /identity/resources/configurations/v1` | [docs](https://developers.frontegg.com/ciam/api/identity/core-settings) |
| [Update MFA Configuration](actions/update-mfa-configuration.md) | `POST /identity/resources/configurations/v1/mfa` | [docs](https://developers.frontegg.com/ciam/api/identity/mfa-configuration) |
| [Update Permission](actions/update-permission.md) | `PATCH /identity/resources/permissions/v1/:permissionId` | [docs](https://developers.frontegg.com/ciam/api/identity/permissions) |
| [Update Tenant](actions/update-tenant.md) | `PUT /tenants/resources/tenants/v2/:tenantId` | [docs](https://developers.frontegg.com/ciam/api/tenants/accounts) |
| [Update User](actions/update-user.md) | `PUT /identity/resources/users/v1/:userId` | [docs](https://developers.frontegg.com/ciam/api/identity/user-management) |
| [Verify User](actions/verify-user.md) | `POST /identity/resources/users/v1/:userId/verify` | [docs](https://developers.frontegg.com/ciam/api/identity/users) |
