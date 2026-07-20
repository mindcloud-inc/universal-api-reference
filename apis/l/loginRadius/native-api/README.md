# LoginRadius: Native API Reference

A consolidated summary of LoginRadius's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.loginradius.com/docs/api/openapi/customer-identity-api/
- **API base URL:** `https://api.loginradius.com`

## Authentication

### API Key

Use the LoginRadius API key and API secret from Tenant Settings > API Configuration.

### Credentials

- **API Key:** `apiKey` · required
- **API Secret:** `apiSecret` · required · Primary or scoped API secret from Tenant Settings > API Configuration.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.loginradius.com/docs/tenant-management/tenant-configuration/api-configuration/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Email](actions/add-email.md) | `POST /identity/v2/auth/email` | [docs](https://www.loginradius.com/docs/api/openapi/add-email/) |
| [Assign Roles in Organization](actions/assign-roles-in-organization.md) | `PUT /v2/manage/account/:uid/orgcontext/:orgId/roles` | [docs](https://www.loginradius.com/docs/api/openapi/assign-roles-to-user/) |
| [Change Phone Number](actions/change-phone-number.md) | `PUT /identity/v2/auth/phone` | [docs](https://www.loginradius.com/docs/api/openapi/change-phone-number/) |
| [Check Email Availability](actions/check-email-availability.md) | `GET /identity/v2/auth/email` | [docs](https://www.loginradius.com/docs/api/openapi/check-email-availability/) |
| [Create Account](actions/create-account.md) | `POST /identity/v2/manage/account` | [docs](https://www.loginradius.com/docs/api/openapi/create-user/) |
| [Create Custom Object](actions/create-custom-object.md) | `POST /identity/v2/auth/customobject` | [docs](https://www.loginradius.com/docs/api/openapi/create-custom-object-by-token/) |
| [Create Organization](actions/create-organization.md) | `POST /v2/manage/organizations` | [docs](https://www.loginradius.com/docs/api/openapi/create-organization/) |
| [Create Organization Connection](actions/create-organization-connection.md) | `POST /v2/manage/organizations/:orgId/connections` | [docs](https://www.loginradius.com/docs/api/openapi/create-organization-connection/) |
| [Create Role](actions/create-role.md) | `POST /identity/v2/manage/role` | [docs](https://www.loginradius.com/docs/api/openapi/create-role/) |
| [Create Webhook Configuration](actions/create-webhook-configuration.md) | `POST /v2/manage/webhooks` | [docs](https://www.loginradius.com/docs/api/openapi/create-webhook-configuration/) |
| [Delete Account by Email](actions/delete-account-by-email.md) | `DELETE /identity/v2/manage/account` | [docs](https://www.loginradius.com/docs/api/openapi/delete-account-by-email/) |
| [Delete Account by UID](actions/delete-account-by-uid.md) | `DELETE /identity/v2/manage/account/:uid` | [docs](https://www.loginradius.com/docs/api/openapi/delete-account-by-uid/) |
| [Delete Custom Object by ID](actions/delete-custom-object-by-id.md) | `DELETE /identity/v2/auth/customobject/:objectrecordid` | [docs](https://www.loginradius.com/docs/api/openapi/delete-custom-object-by-token-and-record-id/) |
| [Forgot Password](actions/forgot-password.md) | `POST /identity/v2/auth/password` | [docs](https://www.loginradius.com/docs/api/openapi/forgot-password/) |
| [Generate Backup Codes](actions/generate-backup-codes.md) | `GET /identity/v2/auth/account/2fa/backupcode` | [docs](https://www.loginradius.com/docs/api/openapi/mfa-generate-backup-codes/) |
| [Get Server Time](actions/get-server-time.md) | `GET /identity/v2/serverinfo` | [docs](https://www.loginradius.com/docs/api/v2/customer-identity-api/configuration/get-server-time/) |
| [Invalidate Access Token](actions/invalidate-access-token.md) | `GET /identity/v2/auth/access_token/invalidate` | [docs](https://www.loginradius.com/docs/api/openapi/invalidate-access-token/) |
| [List Organization Connections](actions/list-organization-connections.md) | `GET /v2/manage/organizations/:orgId/connections` | [docs](https://www.loginradius.com/docs/api/openapi/get-all-organization-connections/) |
| [List Organizations](actions/list-organizations.md) | `GET /v2/manage/organizations` | [docs](https://www.loginradius.com/docs/api/openapi/get-all-organizations/) |
| [List Roles](actions/list-roles.md) | `GET /identity/v2/manage/role` | [docs](https://www.loginradius.com/docs/api/openapi/get-all-roles/) |
| [List User Profiles](actions/list-user-profiles.md) | `GET https://cloud-api.loginradius.com/identity` | [docs](https://www.loginradius.com/docs/api/openapi/get-user-profiles-by-page-id/) |
| [List Webhook Configurations](actions/list-webhook-configurations.md) | `GET /v2/manage/webhooks` | [docs](https://www.loginradius.com/docs/api/openapi/get-all-webhooks-configurations/) |
| [Login With Credentials](actions/login-with-credentials.md) | `POST /identity/v2/auth/login` | [docs](https://www.loginradius.com/docs/api/openapi/email-by-login-user-name-phone/) |
| [MFA Login](actions/mfa-login.md) | `POST /identity/v2/auth/login/2fa` | [docs](https://www.loginradius.com/docs/api/openapi/mfa-login/) |
| [Query Custom Objects](actions/query-custom-objects.md) | `POST https://cloud-api.loginradius.com/customobject` | [docs](https://www.loginradius.com/docs/api/openapi/get-all-custom-objects-by-query/) |
| [Resend Verification Email](actions/resend-verification-email.md) | `PUT /identity/v2/auth/register` | [docs](https://www.loginradius.com/docs/api/openapi/resend-email-verification/) |
| [Reset Backup Codes](actions/reset-backup-codes.md) | `GET /identity/v2/auth/account/2fa/backupcode/reset` | [docs](https://www.loginradius.com/docs/api/openapi/mfa-reset-backup-codes/) |
| [Retrieve Access Token Information](actions/retrieve-access-token-information.md) | `GET /identity/v2/auth/access_token` | [docs](https://www.loginradius.com/docs/api/openapi/get-access-token/) |
| [Retrieve Account](actions/retrieve-account.md) | `GET /identity/v2/manage/account` | [docs](https://www.loginradius.com/docs/api/openapi/get-account-identity/) |
| [Retrieve Account by UID](actions/retrieve-account-by-uid.md) | `GET /identity/v2/manage/account/:uid` | [docs](https://www.loginradius.com/docs/api/openapi/get-account-identity-by-uid/) |
| [Retrieve Active Session](actions/retrieve-active-session.md) | `GET /api/v2/access_token/activesession` | [docs](https://www.loginradius.com/docs/api/openapi/get-active-session/) |
| [Retrieve Custom Objects](actions/retrieve-custom-objects.md) | `GET /identity/v2/auth/customobject` | [docs](https://www.loginradius.com/docs/api/openapi/get-custom-object-by-token/) |
| [Retrieve MFA Settings](actions/retrieve-mfa-settings.md) | `GET /identity/v2/auth/account/2fa` | [docs](https://www.loginradius.com/docs/api/openapi/get-mfa-settings/) |
| [Retrieve Organization Details](actions/retrieve-organization-details.md) | `GET /v2/manage/organizations/:orgId` | [docs](https://www.loginradius.com/docs/api/openapi/get-organization/) |
| [Retrieve Role by ID](actions/retrieve-role-by-id.md) | `GET /v2/manage/roles/:id` | [docs](https://www.loginradius.com/docs/api/openapi/get-role-by-id/) |
| [Retrieve Roles by UID](actions/retrieve-roles-by-uid.md) | `GET /identity/v2/manage/account/:uid/role` | [docs](https://www.loginradius.com/docs/api/openapi/get-roles-by-uid/) |
| [Retrieve User](actions/retrieve-user.md) | `GET /identity/v2/auth/account` | [docs](https://www.loginradius.com/docs/api/openapi/get-account-details/) |
| [Send User Deletion Email](actions/send-user-deletion-email.md) | `DELETE /identity/v2/auth/account` | [docs](https://www.loginradius.com/docs/api/openapi/deleteccountbyaccesstoken/) |
| [Update Password](actions/update-password.md) | `PUT /identity/v2/auth/password/change` | [docs](https://www.loginradius.com/docs/api/openapi/change-password/) |
| [Verify Email](actions/verify-email.md) | `PUT /identity/v2/auth/email` | [docs](https://www.loginradius.com/docs/api/openapi/update-email/) |
