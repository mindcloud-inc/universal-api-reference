# <img src="https://images.mindcloud.co/apps/icons/login-radius_1775064856038.png" alt="LoginRadius logo" width="28" height="28"> LoginRadius: Universal API

Manage customer identities, authentication, and access security

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/loginRadius/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.loginradius.com
- **Vendor API docs:** https://www.loginradius.com/docs/api/openapi/customer-identity-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Server Time](actions/get-server-time.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/get-server-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Invalidate Access Token](actions/invalidate-access-token.md) | DELETE | Invalidates an access token in LoginRadius. |

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Login With Credentials](actions/login-with-credentials.md) | POST | Creates a LoginRadius access token from user credentials. |
| [Retrieve Access Token Information](actions/retrieve-access-token-information.md) | GET | Retrieves access token details from LoginRadius. |

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Delete Account by Email](actions/delete-account-by-email.md) | DELETE | Deletes an existing account from LoginRadius by email. |
| [Delete Account by UID](actions/delete-account-by-uid.md) | DELETE | Deletes an existing account from LoginRadius by UID. |
| [Retrieve Account](actions/retrieve-account.md) | GET | Retrieves an account from LoginRadius by email, username, or phone. |
| [Retrieve Account by UID](actions/retrieve-account-by-uid.md) | GET | Retrieves an account from LoginRadius by UID. |

### Account Deletion Request

| Action | Method | Description |
| --- | --- | --- |
| [Send User Deletion Email](actions/send-user-deletion-email.md) | DELETE | Sends a user deletion email from LoginRadius. |

### Backup Codes

| Action | Method | Description |
| --- | --- | --- |
| [Generate Backup Codes](actions/generate-backup-codes.md) | GET | Retrieves MFA backup codes from LoginRadius. |
| [Reset Backup Codes](actions/reset-backup-codes.md) | PUT | Resets MFA backup codes in LoginRadius. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST | Creates a new organization in LoginRadius. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organization records from a LoginRadius tenant. |
| [Retrieve Organization Details](actions/retrieve-organization-details.md) | GET | Retrieves organization details from your LoginRadius tenant. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization Connection](actions/create-organization-connection.md) | POST | Creates a new organization connection in LoginRadius. |
| [List Organization Connections](actions/list-organization-connections.md) | GET | Retrieves organization connection records from LoginRadius. |

### Custom Object

| Action | Method | Description |
| --- | --- | --- |
| [Delete Custom Object by ID](actions/delete-custom-object-by-id.md) | DELETE | Deletes an existing custom object from LoginRadius by ID. |
| [Query Custom Objects](actions/query-custom-objects.md) | GET | Retrieves custom object records from LoginRadius by query. |

### Email Availability

| Action | Method | Description |
| --- | --- | --- |
| [Check Email Availability](actions/check-email-availability.md) | GET | Checks whether an email is available in LoginRadius. |

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | PUT | Verifies an email address in LoginRadius. |

### Mfa Login

| Action | Method | Description |
| --- | --- | --- |
| [MFA Login](actions/mfa-login.md) | GET | Creates a LoginRadius access token with MFA. |

### Mfa Settings

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve MFA Settings](actions/retrieve-mfa-settings.md) | GET | Retrieves MFA account settings from LoginRadius. |

### Password

| Action | Method | Description |
| --- | --- | --- |
| [Update Password](actions/update-password.md) | PUT | Updates an existing password in LoginRadius. |

### Password Recovery

| Action | Method | Description |
| --- | --- | --- |
| [Forgot Password](actions/forgot-password.md) | PUT | Sends a password reset request in LoginRadius. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Change Phone Number](actions/change-phone-number.md) | PUT | Updates a phone number in LoginRadius. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Roles by UID](actions/retrieve-roles-by-uid.md) | GET | Retrieves assigned roles from LoginRadius by UID. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Assign Roles in Organization](actions/assign-roles-in-organization.md) | PUT | Updates a user's organization roles in LoginRadius. |
| [Create Role](actions/create-role.md) | POST | Creates a new role in LoginRadius. |
| [List Roles](actions/list-roles.md) | GET | Retrieves available role records from LoginRadius. |
| [Retrieve Role by ID](actions/retrieve-role-by-id.md) | GET | Retrieves a role from LoginRadius by ID. |

### Server Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Server Time](actions/get-server-time.md) | GET | Retrieves current server time from LoginRadius. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Active Session](actions/retrieve-active-session.md) | GET | Retrieves an active session from LoginRadius by access token. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Object](actions/create-custom-object.md) | POST | Creates a new custom object in LoginRadius. |
| [Retrieve Custom Objects](actions/retrieve-custom-objects.md) | GET | Retrieves custom object records from LoginRadius. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [List User Profiles](actions/list-user-profiles.md) | GET | Retrieves user profiles from LoginRadius by page. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add Email](actions/add-email.md) | POST | Adds an email address to a LoginRadius account. |
| [Create Account](actions/create-account.md) | POST | Creates a new account in LoginRadius. |
| [Resend Verification Email](actions/resend-verification-email.md) | PUT | Resends an email verification message from LoginRadius. |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves a user profile from LoginRadius. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Configuration](actions/create-webhook-configuration.md) | POST | Creates a new webhook configuration in LoginRadius. |
| [List Webhook Configurations](actions/list-webhook-configurations.md) | GET | Retrieves webhook configurations from your LoginRadius tenant. |

