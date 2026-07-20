# WorkOS: Native API Reference

A consolidated summary of WorkOS's API configuration and 60 documented operations, with links to official documentation.

- **Official docs:** https://workos.com/docs/reference
- **OpenAPI specification:** https://raw.githubusercontent.com/workos/openapi-spec/main/spec/open-api-spec.yaml
- **API base URL:** `https://api.workos.com`

## Authentication

### API Key

Authenticate to WorkOS with an API key. The platform stores the key once as an apiKey secret and sends it as Authorization: Bearer <apiKey>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://workos.com/docs/reference/api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The next-page cursor is read from `list_metadata.after`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `after` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (60 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign a role](actions/assign-a-role.md) | `POST /authorization/organization_memberships/{organization_membership_id}/role_assignments` | [docs](https://workos.com/docs/reference) |
| [Check authorization](actions/check-authorization.md) | `POST /authorization/organization_memberships/{organization_membership_id}/check` | [docs](https://workos.com/docs/reference) |
| [Create a password reset token](actions/create-a-password-reset-token.md) | `POST /user_management/password_reset` | [docs](https://workos.com/docs/reference) |
| [Create a permission](actions/create-a-permission.md) | `POST /authorization/permissions` | [docs](https://workos.com/docs/reference) |
| [Create a user](actions/create-a-user.md) | `POST /user_management/users` | [docs](https://workos.com/docs/reference) |
| [Create a Webhook Endpoint](actions/create-a-webhook-endpoint.md) | `POST /webhook_endpoints` | [docs](https://workos.com/docs/reference) |
| [Create an Organization](actions/create-an-organization.md) | `POST /organizations` | [docs](https://workos.com/docs/reference) |
| [Create an Organization Domain](actions/create-an-organization-domain.md) | `POST /organization_domains` | [docs](https://workos.com/docs/reference) |
| [Create an organization membership](actions/create-an-organization-membership.md) | `POST /user_management/organization_memberships` | [docs](https://workos.com/docs/reference) |
| [Deactivate an organization membership](actions/deactivate-an-organization-membership.md) | `PUT /user_management/organization_memberships/{id}/deactivate` | [docs](https://workos.com/docs/reference) |
| [Delete a Connection](actions/delete-a-connection.md) | `DELETE /connections/{id}` | [docs](https://workos.com/docs/reference) |
| [Delete a user](actions/delete-a-user.md) | `DELETE /user_management/users/{id}` | [docs](https://workos.com/docs/reference) |
| [Delete a Webhook Endpoint](actions/delete-a-webhook-endpoint.md) | `DELETE /webhook_endpoints/{id}` | [docs](https://workos.com/docs/reference) |
| [Delete an Organization Domain](actions/delete-an-organization-domain.md) | `DELETE /organization_domains/{id}` | [docs](https://workos.com/docs/reference) |
| [Delete an organization membership](actions/delete-an-organization-membership.md) | `DELETE /user_management/organization_memberships/{id}` | [docs](https://workos.com/docs/reference) |
| [Get a Connection](actions/get-a-connection.md) | `GET /connections/{id}` | [docs](https://workos.com/docs/reference) |
| [Get a Directory](actions/get-a-directory.md) | `GET /directories/{id}` | [docs](https://workos.com/docs/reference) |
| [Get a Directory Group](actions/get-a-directory-group.md) | `GET /directory_groups/{id}` | [docs](https://workos.com/docs/reference) |
| [Get a Directory User](actions/get-a-directory-user.md) | `GET /directory_users/{id}` | [docs](https://workos.com/docs/reference) |
| [Get a feature flag](actions/get-a-feature-flag.md) | `GET /feature-flags/{slug}` | [docs](https://workos.com/docs/reference) |
| [Get a password reset token](actions/get-a-password-reset-token.md) | `GET /user_management/password_reset/{id}` | [docs](https://workos.com/docs/reference) |
| [Get a permission](actions/get-a-permission.md) | `GET /authorization/permissions/{slug}` | [docs](https://workos.com/docs/reference) |
| [Get a user](actions/get-a-user.md) | `GET /user_management/users/{id}` | [docs](https://workos.com/docs/reference) |
| [Get a user by external ID](actions/get-a-user-by-external-id.md) | `GET /user_management/users/external_id/{external_id}` | [docs](https://workos.com/docs/reference) |
| [Get an invitation](actions/get-an-invitation.md) | `GET /user_management/invitations/{id}` | [docs](https://workos.com/docs/reference) |
| [Get an Organization](actions/get-an-organization.md) | `GET /organizations/{id}` | [docs](https://workos.com/docs/reference) |
| [Get an Organization by External ID](actions/get-an-organization-by-external-id.md) | `GET /organizations/external_id/{external_id}` | [docs](https://workos.com/docs/reference) |
| [Get an Organization Domain](actions/get-an-organization-domain.md) | `GET /organization_domains/{id}` | [docs](https://workos.com/docs/reference) |
| [Get an organization membership](actions/get-an-organization-membership.md) | `GET /user_management/organization_memberships/{id}` | [docs](https://workos.com/docs/reference) |
| [Get Audit Log Configuration](actions/get-audit-log-configuration.md) | `GET /organizations/{id}/audit_log_configuration` | [docs](https://workos.com/docs/reference) |
| [Get Retention](actions/get-retention.md) | `GET /organizations/{id}/audit_logs_retention` | [docs](https://workos.com/docs/reference) |
| [Get user identities](actions/get-user-identities.md) | `GET /user_management/users/{id}/identities` | [docs](https://workos.com/docs/reference) |
| [List Connections](actions/list-connections.md) | `GET /connections` | [docs](https://workos.com/docs/reference) |
| [List Directories](actions/list-directories.md) | `GET /directories` | [docs](https://workos.com/docs/reference) |
| [List Directory Groups](actions/list-directory-groups.md) | `GET /directory_groups` | [docs](https://workos.com/docs/reference) |
| [List Directory Users](actions/list-directory-users.md) | `GET /directory_users` | [docs](https://workos.com/docs/reference) |
| [List events](actions/list-events.md) | `GET /events` | [docs](https://workos.com/docs/reference) |
| [List feature flags](actions/list-feature-flags.md) | `GET /feature-flags` | [docs](https://workos.com/docs/reference) |
| [List invitations](actions/list-invitations.md) | `GET /user_management/invitations` | [docs](https://workos.com/docs/reference) |
| [List organization memberships](actions/list-organization-memberships.md) | `GET /user_management/organization_memberships` | [docs](https://workos.com/docs/reference) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://workos.com/docs/reference) |
| [List permissions](actions/list-permissions.md) | `GET /authorization/permissions` | [docs](https://workos.com/docs/reference) |
| [List role assignments](actions/list-role-assignments.md) | `GET /authorization/organization_memberships/{organization_membership_id}/role_assignments` | [docs](https://workos.com/docs/reference) |
| [List sessions](actions/list-sessions.md) | `GET /user_management/users/{id}/sessions` | [docs](https://workos.com/docs/reference) |
| [List users](actions/list-users.md) | `GET /user_management/users` | [docs](https://workos.com/docs/reference) |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | `GET /webhook_endpoints` | [docs](https://workos.com/docs/reference) |
| [Reactivate an organization membership](actions/reactivate-an-organization-membership.md) | `PUT /user_management/organization_memberships/{id}/reactivate` | [docs](https://workos.com/docs/reference) |
| [Remove a role assignment](actions/remove-a-role-assignment.md) | `DELETE /authorization/organization_memberships/{organization_membership_id}/role_assignments` | [docs](https://workos.com/docs/reference) |
| [Resend an invitation](actions/resend-an-invitation.md) | `POST /user_management/invitations/{id}/resend` | [docs](https://workos.com/docs/reference) |
| [Revoke an invitation](actions/revoke-an-invitation.md) | `POST /user_management/invitations/{id}/revoke` | [docs](https://workos.com/docs/reference) |
| [Send an invitation](actions/send-an-invitation.md) | `POST /user_management/invitations` | [docs](https://workos.com/docs/reference) |
| [Send verification email](actions/send-verification-email.md) | `POST /user_management/users/{id}/email_verification/send` | [docs](https://workos.com/docs/reference) |
| [Set Retention](actions/set-retention.md) | `PUT /organizations/{id}/audit_logs_retention` | [docs](https://workos.com/docs/reference) |
| [Update a permission](actions/update-a-permission.md) | `PATCH /authorization/permissions/{slug}` | [docs](https://workos.com/docs/reference) |
| [Update a user](actions/update-a-user.md) | `PUT /user_management/users/{id}` | [docs](https://workos.com/docs/reference) |
| [Update a Webhook Endpoint](actions/update-a-webhook-endpoint.md) | `PATCH /webhook_endpoints/{id}` | [docs](https://workos.com/docs/reference) |
| [Update an Organization](actions/update-an-organization.md) | `PUT /organizations/{id}` | [docs](https://workos.com/docs/reference) |
| [Update an organization membership](actions/update-an-organization-membership.md) | `PUT /user_management/organization_memberships/{id}` | [docs](https://workos.com/docs/reference) |
| [Verify an Organization Domain](actions/verify-an-organization-domain.md) | `POST /organization_domains/{id}/verify` | [docs](https://workos.com/docs/reference) |
| [Verify email](actions/verify-email.md) | `POST /user_management/users/{id}/email_verification/confirm` | [docs](https://workos.com/docs/reference) |
