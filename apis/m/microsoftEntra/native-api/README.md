# Microsoft Entra: Native API Reference

A consolidated summary of Microsoft Entra's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/graph/api/overview
- **OpenAPI specification:** https://raw.githubusercontent.com/microsoftgraph/msgraph-metadata/master/openapi/v1.0/openapi.yaml
- **API base URL:** `https://graph.microsoft.com/v1.0`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/organizations/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/organizations/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `offline_access https://graph.microsoft.com/User.ReadWrite.All https://graph.microsoft.com/Directory.ReadWrite.All`.

PKCE is enabled with the `other` challenge method. The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.microsoftonline.com/organizations/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/entra/identity-platform/v2-oauth2-auth-code-flow)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `$top` in the query string to set the page size (default 100; accepted range 1–999). Use `$skiptoken` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Sorting

Set the sort field with `$orderby` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://learn.microsoft.com/en-us/graph/api/group-post-groups?view=graph-rest-1.0) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://learn.microsoft.com/en-us/graph/api/user-post-users?view=graph-rest-1.0) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:userId` | [docs](https://learn.microsoft.com/en-us/graph/api/user-delete?view=graph-rest-1.0) |
| [Get Group](actions/get-group.md) | `GET /groups/:groupId` | [docs](https://learn.microsoft.com/en-us/graph/api/group-get?view=graph-rest-1.0) |
| [Get Organization](actions/get-organization.md) | `GET /organization/:organizationId` | [docs](https://learn.microsoft.com/en-us/graph/api/organization-get?view=graph-rest-1.0) |
| [Get User](actions/get-user.md) | `GET /users/:userId` | [docs](https://learn.microsoft.com/en-us/graph/api/user-get?view=graph-rest-1.0) |
| [Get User Manager](actions/get-user-manager.md) | `GET /users/:userId/manager` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-manager?view=graph-rest-1.0) |
| [List Group Memberships](actions/list-group-memberships.md) | `GET /groups/:groupId/memberOf` | [docs](https://learn.microsoft.com/en-us/graph/api/group-list-memberof?view=graph-rest-1.0) |
| [List Group Transitive Memberships](actions/list-group-transitive-memberships.md) | `GET /groups/:groupId/transitiveMemberOf` | [docs](https://learn.microsoft.com/en-us/graph/api/group-list-transitivememberof?view=graph-rest-1.0) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://learn.microsoft.com/en-us/graph/api/group-list?view=graph-rest-1.0) |
| [List Organizations](actions/list-organizations.md) | `GET /organization` | [docs](https://learn.microsoft.com/en-us/graph/api/organization-list?view=graph-rest-1.0) |
| [List User Direct Reports](actions/list-user-direct-reports.md) | `GET /users/:userId/directReports` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-directreports?view=graph-rest-1.0) |
| [List User Memberships](actions/list-user-memberships.md) | `GET /users/:userId/memberOf` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-memberof?view=graph-rest-1.0) |
| [List User Owned Objects](actions/list-user-owned-objects.md) | `GET /users/:userId/ownedObjects` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-ownedobjects?view=graph-rest-1.0) |
| [List User Transitive Memberships](actions/list-user-transitive-memberships.md) | `GET /users/:userId/transitiveMemberOf` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-transitivememberof?view=graph-rest-1.0) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list?view=graph-rest-1.0) |
| [Remove Group Member](actions/remove-group-member.md) | `DELETE /groups/:groupId/members/:memberId/$ref` | [docs](https://learn.microsoft.com/en-us/graph/api/group-delete-members?view=graph-rest-1.0) |
| [Remove User Manager](actions/remove-user-manager.md) | `DELETE /users/:userId/manager/$ref` | [docs](https://learn.microsoft.com/en-us/graph/api/user-delete-manager?view=graph-rest-1.0) |
| [Set User Manager](actions/set-user-manager.md) | `PUT /users/:userId/manager/$ref` | [docs](https://learn.microsoft.com/en-us/graph/api/user-post-manager?view=graph-rest-1.0) |
| [Update Group](actions/update-group.md) | `PATCH /groups/:groupId` | [docs](https://learn.microsoft.com/en-us/graph/api/group-update?view=graph-rest-1.0) |
| [Update User](actions/update-user.md) | `PATCH /users/:userId` | [docs](https://learn.microsoft.com/en-us/graph/api/user-update?view=graph-rest-1.0) |
