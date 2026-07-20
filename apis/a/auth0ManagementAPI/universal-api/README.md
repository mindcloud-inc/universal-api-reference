# <img src="https://images.mindcloud.co/apps/icons/auth0management-api_1775773481078.png" alt="Auth0 Management logo" width="28" height="28"> Auth0 Management: Universal API

Manage Auth0 users, clients, roles, and organizations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/auth0ManagementAPI/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://auth0.com/
- **Vendor API docs:** https://dev.auth0.com/docs/api/management/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/auth0ManagementAPI/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a client in Auth0 Management API. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes a client from Auth0 Management API. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Auth0 Management API. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Auth0 Management API. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Auth0 Management API. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Delete Organization Connection](actions/delete-organization-connection.md) | DELETE | Deletes a connection from an organization in Auth0 Management API. |
| [Enable Organization Connection](actions/enable-organization-connection.md) | POST | Enables a connection for an organization in Auth0 Management API. |
| [List Organization Connections](actions/list-organization-connections.md) | GET | Retrieves enabled connections for an organization in Auth0 Management API. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST | Creates an organization in Auth0 Management API. |
| [Delete Organization](actions/delete-organization.md) | DELETE | Deletes an organization from Auth0 Management API. |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Auth0 Management API. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Auth0 Management API. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in Auth0 Management API. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [List Role Permissions](actions/list-role-permissions.md) | GET | Retrieves permissions assigned to a role in Auth0 Management API. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Assign User Roles](actions/assign-user-roles.md) | PUT | Assigns roles to a user in Auth0 Management API. |
| [Create Role](actions/create-role.md) | POST | Creates a role in Auth0 Management API. |
| [Delete Role](actions/delete-role.md) | DELETE | Deletes a role from Auth0 Management API. |
| [Get Role](actions/get-role.md) | GET | Retrieves a role from Auth0 Management API. |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from Auth0 Management API. |
| [List User Roles](actions/list-user-roles.md) | GET | Retrieves roles assigned to a user in Auth0 Management API. |
| [Remove User Roles](actions/remove-user-roles.md) | DELETE | Removes roles from a user in Auth0 Management API. |
| [Update Role](actions/update-role.md) | PUT | Updates an existing role in Auth0 Management API. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add Organization Members](actions/add-organization-members.md) | POST | Adds members to an organization in Auth0 Management API. |
| [Create User](actions/create-user.md) | POST | Creates a user in Auth0 Management API. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from Auth0 Management API. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Auth0 Management API. |
| [List Organization Members](actions/list-organization-members.md) | GET | Retrieves members of an organization in Auth0 Management API. |
| [List Role Users](actions/list-role-users.md) | GET | Retrieves users assigned to a role in Auth0 Management API. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Auth0 Management API. |
| [Remove Organization Members](actions/remove-organization-members.md) | DELETE | Removes members from an organization in Auth0 Management API. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Auth0 Management API. |

