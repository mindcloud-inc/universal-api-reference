# <img src="https://images.mindcloud.co/apps/icons/permitio-icon_1775747382600.png" alt="Permit.io logo" width="28" height="28"> Permit.io: Universal API

Manage authorization policies, roles, users, and tenant access

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/permitio/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://permit.io
- **Vendor API docs:** https://api.permit.io/scalar

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Key Scope](actions/get-api-key-scope.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/permitio/latest/actions/get-api-key-scope?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Api Key Scope

| Action | Method | Description |
| --- | --- | --- |
| [Get API Key Scope](actions/get-api-key-scope.md) | GET |  |

### Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [List Audit Logs](actions/list-audit-logs.md) | GET |  |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [List Environments](actions/list-environments.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Create Resource](actions/create-resource.md) | POST |  |
| [Get Resource](actions/get-resource.md) | GET |  |
| [List Resources](actions/list-resources.md) | GET |  |
| [Update Resource](actions/update-resource.md) | PUT |  |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/create-role.md) | POST |  |
| [Get Role](actions/get-role.md) | GET |  |
| [List Roles](actions/list-roles.md) | GET |  |
| [Update Role](actions/update-role.md) | PUT |  |

### Role Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Assign Role](actions/assign-role.md) | POST |  |
| [List Role Assignments](actions/list-role-assignments.md) | GET |  |

### Tenant

| Action | Method | Description |
| --- | --- | --- |
| [Create Tenant](actions/create-tenant.md) | POST |  |
| [Get Tenant](actions/get-tenant.md) | GET |  |
| [List Tenants](actions/list-tenants.md) | GET |  |
| [Update Tenant](actions/update-tenant.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Update User](actions/update-user.md) | PUT |  |

