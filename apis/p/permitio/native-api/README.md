# Permit.io: Native API Reference

A consolidated summary of Permit.io's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.permit.io/scalar
- **OpenAPI specification:** https://api.permit.io/v2/openapi.json
- **API base URL:** `https://api.permit.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.permit.io/overview/use-the-permit-api-and-sdk/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size (default 30; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Role](actions/assign-role.md) | `POST /v2/facts/:projId/:envId/role_assignments` | [docs](https://api.permit.io/scalar) |
| [Create Resource](actions/create-resource.md) | `POST /v2/schema/:projId/:envId/resources` | [docs](https://api.permit.io/scalar) |
| [Create Role](actions/create-role.md) | `POST /v2/schema/:projId/:envId/roles` | [docs](https://api.permit.io/scalar) |
| [Create Tenant](actions/create-tenant.md) | `POST /v2/facts/:projId/:envId/tenants` | [docs](https://api.permit.io/scalar) |
| [Create User](actions/create-user.md) | `POST /v2/facts/:projId/:envId/users` | [docs](https://api.permit.io/scalar) |
| [Get API Key Scope](actions/get-api-key-scope.md) | `GET /v2/api-key/scope` | [docs](https://api.permit.io/scalar) |
| [Get Project](actions/get-project.md) | `GET /v2/projects/:projId` | [docs](https://api.permit.io/scalar) |
| [Get Resource](actions/get-resource.md) | `GET /v2/schema/:projId/:envId/resources/:resourceId` | [docs](https://api.permit.io/scalar) |
| [Get Role](actions/get-role.md) | `GET /v2/schema/:projId/:envId/roles/:roleId` | [docs](https://api.permit.io/scalar) |
| [Get Tenant](actions/get-tenant.md) | `GET /v2/facts/:projId/:envId/tenants/:tenantId` | [docs](https://api.permit.io/scalar) |
| [Get User](actions/get-user.md) | `GET /v2/facts/:projId/:envId/users/:userId` | [docs](https://api.permit.io/scalar) |
| [List Audit Logs](actions/list-audit-logs.md) | `GET /v2/pdps/:projId/:envId/audit_logs` | [docs](https://api.permit.io/scalar) |
| [List Environments](actions/list-environments.md) | `GET /v2/projects/:projId/envs` | [docs](https://api.permit.io/scalar) |
| [List Organizations](actions/list-organizations.md) | `GET /v2/orgs` | [docs](https://api.permit.io/scalar) |
| [List Projects](actions/list-projects.md) | `GET /v2/projects` | [docs](https://api.permit.io/scalar) |
| [List Resources](actions/list-resources.md) | `GET /v2/schema/:projId/:envId/resources` | [docs](https://api.permit.io/scalar) |
| [List Role Assignments](actions/list-role-assignments.md) | `GET /v2/facts/:projId/:envId/role_assignments` | [docs](https://api.permit.io/scalar) |
| [List Roles](actions/list-roles.md) | `GET /v2/schema/:projId/:envId/roles` | [docs](https://api.permit.io/scalar) |
| [List Tenants](actions/list-tenants.md) | `GET /v2/facts/:projId/:envId/tenants` | [docs](https://api.permit.io/scalar) |
| [List Users](actions/list-users.md) | `GET /v2/facts/:projId/:envId/users` | [docs](https://api.permit.io/scalar) |
| [Update Resource](actions/update-resource.md) | `PATCH /v2/schema/:projId/:envId/resources/:resourceId` | [docs](https://api.permit.io/scalar) |
| [Update Role](actions/update-role.md) | `PATCH /v2/schema/:projId/:envId/roles/:roleId` | [docs](https://api.permit.io/scalar) |
| [Update Tenant](actions/update-tenant.md) | `PATCH /v2/facts/:projId/:envId/tenants/:tenantId` | [docs](https://api.permit.io/scalar) |
| [Update User](actions/update-user.md) | `PATCH /v2/facts/:projId/:envId/users/:userId` | [docs](https://api.permit.io/scalar) |
