# <img src="https://images.mindcloud.co/apps/icons/workos-icon_1776883969672.png" alt="WorkOS logo" width="28" height="28"> WorkOS: Universal API

WorkOS provides enterprise-ready APIs for user management, organizations, SSO, directory sync, audit logs, RBAC authorization, feature flags, webhooks, Radar risk checks, and related administrative workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/workOS/latest
- **Actions:** 60
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://workos.com
- **Vendor API docs:** https://workos.com/docs/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (60)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Create a password reset token](actions/create-a-password-reset-token.md) | POST | Creates a password reset token in your WorkOS environment. |
| [Get a password reset token](actions/get-a-password-reset-token.md) | GET | Retrieves a password reset token from your WorkOS environment. |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Delete a Connection](actions/delete-a-connection.md) | DELETE | Deletes a connection from your WorkOS environment. |
| [Get a Connection](actions/get-a-connection.md) | GET | Retrieves a connection from your WorkOS environment. |
| [List Connections](actions/list-connections.md) | GET | Retrieves connections from your WorkOS environment. |

### Data Source

| Action | Method | Description |
| --- | --- | --- |
| [Get a Directory](actions/get-a-directory.md) | GET | Retrieves a directory from your WorkOS environment. |
| [List Directories](actions/list-directories.md) | GET | Retrieves directories from your WorkOS environment. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Send verification email](actions/send-verification-email.md) | POST | Sends a verification email in your WorkOS environment. |
| [Verify email](actions/verify-email.md) | POST | Verifies an email in your WorkOS environment. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List events](actions/list-events.md) | GET | Retrieves events from your WorkOS environment. |

### Feature Request

| Action | Method | Description |
| --- | --- | --- |
| [Get a feature flag](actions/get-a-feature-flag.md) | GET | Retrieves a feature flag from your WorkOS environment. |
| [List feature flags](actions/list-feature-flags.md) | GET | Retrieves feature flags from your WorkOS environment. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get a Directory Group](actions/get-a-directory-group.md) | GET | Retrieves a directory group from your WorkOS environment. |
| [List Directory Groups](actions/list-directory-groups.md) | GET | Retrieves directory groups from your WorkOS environment. |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [Get an invitation](actions/get-an-invitation.md) | GET | Retrieves an invitation from your WorkOS environment. |
| [List invitations](actions/list-invitations.md) | GET | Retrieves invitations from your WorkOS environment. |
| [Resend an invitation](actions/resend-an-invitation.md) | POST | Resends an invitation in your WorkOS environment. |
| [Revoke an invitation](actions/revoke-an-invitation.md) | POST | Revokes an invitation in your WorkOS environment. |
| [Send an invitation](actions/send-an-invitation.md) | POST | Sends an invitation in your WorkOS environment. |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [Create an organization membership](actions/create-an-organization-membership.md) | POST | Creates an organization membership in your WorkOS environment. |
| [Deactivate an organization membership](actions/deactivate-an-organization-membership.md) | PUT | Deactivates an organization membership in your WorkOS environment. |
| [Delete an organization membership](actions/delete-an-organization-membership.md) | DELETE | Deletes an organization membership from your WorkOS environment. |
| [Get an organization membership](actions/get-an-organization-membership.md) | GET | Retrieves an organization membership from your WorkOS environment. |
| [List organization memberships](actions/list-organization-memberships.md) | GET | Retrieves organization memberships from your WorkOS environment. |
| [Reactivate an organization membership](actions/reactivate-an-organization-membership.md) | PUT | Reactivates an organization membership in your WorkOS environment. |
| [Update an organization membership](actions/update-an-organization-membership.md) | PUT | Updates an organization membership in your WorkOS environment. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create an Organization](actions/create-an-organization.md) | POST | Creates an organization in your WorkOS environment. |
| [Create an Organization Domain](actions/create-an-organization-domain.md) | POST | Creates an organization domain in your WorkOS environment. |
| [Delete an Organization Domain](actions/delete-an-organization-domain.md) | DELETE | Deletes an organization domain from your WorkOS environment. |
| [Get an Organization](actions/get-an-organization.md) | GET | Retrieves an organization from your WorkOS environment. |
| [Get an Organization by External ID](actions/get-an-organization-by-external-id.md) | GET | Retrieves an organization by external ID from your WorkOS environment. |
| [Get an Organization Domain](actions/get-an-organization-domain.md) | GET | Retrieves an organization domain from your WorkOS environment. |
| [Get Audit Log Configuration](actions/get-audit-log-configuration.md) | GET | Retrieves audit log configuration from your WorkOS environment. |
| [Get Retention](actions/get-retention.md) | GET | Retrieves retention from your WorkOS environment. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from your WorkOS environment. |
| [Set Retention](actions/set-retention.md) | PUT | Sets retention in your WorkOS environment. |
| [Update an Organization](actions/update-an-organization.md) | PUT | Updates an organization in your WorkOS environment. |
| [Verify an Organization Domain](actions/verify-an-organization-domain.md) | POST | Verifies an organization domain in your WorkOS environment. |

### Permission

| Action | Method | Description |
| --- | --- | --- |
| [Check authorization](actions/check-authorization.md) | POST | Checks authorization in your WorkOS environment. |
| [Create a permission](actions/create-a-permission.md) | POST | Creates a permission in your WorkOS environment. |
| [Get a permission](actions/get-a-permission.md) | GET | Retrieves a permission from your WorkOS environment. |
| [List permissions](actions/list-permissions.md) | GET | Retrieves permissions from your WorkOS environment. |
| [Update a permission](actions/update-a-permission.md) | PUT | Updates a permission in your WorkOS environment. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Assign a role](actions/assign-a-role.md) | POST | Assigns a role in your WorkOS environment. |
| [List role assignments](actions/list-role-assignments.md) | GET | Retrieves role assignments from your WorkOS environment. |
| [Remove a role assignment](actions/remove-a-role-assignment.md) | DELETE | Removes a role assignment from your WorkOS environment. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [List sessions](actions/list-sessions.md) | GET | Retrieves sessions from your WorkOS environment. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create a user](actions/create-a-user.md) | POST | Creates a user in your WorkOS environment. |
| [Delete a user](actions/delete-a-user.md) | DELETE | Deletes a user from your WorkOS environment. |
| [Get a Directory User](actions/get-a-directory-user.md) | GET | Retrieves a directory user from your WorkOS environment. |
| [Get a user](actions/get-a-user.md) | GET | Retrieves a user from your WorkOS environment. |
| [Get a user by external ID](actions/get-a-user-by-external-id.md) | GET | Retrieves a user by external ID from your WorkOS environment. |
| [Get user identities](actions/get-user-identities.md) | GET | Retrieves user identities from your WorkOS environment. |
| [List Directory Users](actions/list-directory-users.md) | GET | Retrieves directory users from your WorkOS environment. |
| [List users](actions/list-users.md) | GET | Retrieves users from your WorkOS environment. |
| [Update a user](actions/update-a-user.md) | PUT | Updates a user in your WorkOS environment. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create a Webhook Endpoint](actions/create-a-webhook-endpoint.md) | POST | Creates a webhook endpoint in your WorkOS environment. |
| [Delete a Webhook Endpoint](actions/delete-a-webhook-endpoint.md) | DELETE | Deletes a webhook endpoint from your WorkOS environment. |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | GET | Retrieves webhook endpoints from your WorkOS environment. |
| [Update a Webhook Endpoint](actions/update-a-webhook-endpoint.md) | PUT | Updates a webhook endpoint in your WorkOS environment. |

