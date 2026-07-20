# <img src="https://images.mindcloud.co/apps/icons/frontegg_1776198582339.png" alt="Frontegg logo" width="28" height="28"> Frontegg: Universal API

Manage authentication, users, and identity settings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/frontegg/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://frontegg.com
- **Vendor API docs:** https://developers.frontegg.com/ciam/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Identity Management Configuration](actions/get-identity-management-configuration.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-identity-management-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Add Roles To Group](actions/add-roles-to-group.md) | PUT | Adds roles to a user group in Frontegg. |
| [Add Users To Group](actions/add-users-to-group.md) | PUT | Adds users to a user group in Frontegg. |
| [Create Group](actions/create-group.md) | POST | Creates a new user group in Frontegg. |
| [List Groups](actions/list-groups.md) | GET | Finds user groups for a Frontegg account. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing user group in Frontegg. |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Invite For User](actions/create-account-invite-for-user.md) | POST | Creates an account invitation for a user in Frontegg. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Captcha Policy](actions/get-captcha-policy.md) | GET | Retrieves the CAPTCHA policy from Frontegg. |
| [Get Domain Restrictions](actions/get-domain-restrictions.md) | GET | Retrieves domain restrictions for a Frontegg account. |
| [Get Environment Token](actions/get-environment-token.md) | POST | Retrieves a management token for your Frontegg environment. |
| [Get Identity Management Configuration](actions/get-identity-management-configuration.md) | GET | Retrieves identity management configuration from Frontegg. |
| [Get MFA Configuration](actions/get-mfa-configuration.md) | GET | Retrieves MFA configuration for your Frontegg environment. |
| [Update Identity Management Configuration](actions/update-identity-management-configuration.md) | PUT | Updates identity management configuration in Frontegg. |
| [Update MFA Configuration](actions/update-mfa-configuration.md) | PUT | Updates MFA configuration for your Frontegg environment. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [Create Permission](actions/create-permission.md) | POST | Creates a new permission in Frontegg. |
| [List Permissions](actions/list-permissions.md) | GET | Finds permissions in your Frontegg environment. |
| [Set Permission Roles](actions/set-permission-roles.md) | PUT | Updates the roles assigned to a permission in Frontegg. |
| [Update Permission](actions/update-permission.md) | PUT | Updates an existing permission in Frontegg. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/create-role.md) | POST | Creates a new role in Frontegg. |
| [List Roles](actions/list-roles.md) | GET | Finds roles in your Frontegg environment. |

### Tenant

| Action | Method | Description |
| --- | --- | --- |
| [Create Tenant](actions/create-tenant.md) | POST | Creates a new account in Frontegg. |
| [Get Tenant](actions/get-tenant.md) | GET | Retrieves an account in Frontegg by ID. |
| [List Tenants](actions/list-tenants.md) | GET | Finds accounts in your Frontegg environment. |
| [Update Tenant](actions/update-tenant.md) | PUT | Updates an existing account in Frontegg. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Tenant](actions/add-user-to-tenant.md) | PUT | Adds a user to an account in Frontegg. |
| [Create User](actions/create-user.md) | POST | Creates a new user in Frontegg. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from Frontegg. |
| [Disable User Account (Tenant)](actions/disable-user-account-tenant.md) | PUT | Disables a user for an account in Frontegg. |
| [Enable User Account (Tenant)](actions/enable-user-account-tenant.md) | PUT | Enables a user for an account in Frontegg. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Frontegg by ID. |
| [List Users](actions/list-users.md) | GET | Finds users in your Frontegg environment. |
| [Lock User](actions/lock-user.md) | PUT | Updates a user's lock status in Frontegg. |
| [Move Users Between Tenants](actions/move-users-between-tenants.md) | PUT | Moves users between accounts in Frontegg. |
| [Unlock User](actions/unlock-user.md) | PUT | Unlocks a locked user in Frontegg. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Frontegg. |
| [Verify User](actions/verify-user.md) | PUT | Marks a user as verified in Frontegg. |

