# <img src="https://images.mindcloud.co/apps/icons/last-pass_1774458047005.png" alt="LastPass logo" width="28" height="28"> LastPass: Universal API

Manage LastPass users, groups, and shared folder access

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lastPass/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lastpass.com
- **Vendor API docs:** https://support.lastpass.com/help/use-the-lastpass-enterprise-api-postman-collection

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Detailed Shared Folder Data](actions/get-detailed-shared-folder-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/get-detailed-shared-folder-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Reporting Data](actions/get-reporting-data.md) | GET | Retrieves reporting data from LastPass. |

### Shared Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get Detailed Shared Folder Data](actions/get-detailed-shared-folder-data.md) | GET | Retrieves detailed shared folder data from LastPass. |
| [Get Shared Folder Data](actions/get-shared-folder-data.md) | GET | Retrieves shared folder data from LastPass. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in LastPass. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from LastPass. |
| [Get User Data](actions/get-user-data.md) | GET | Retrieves user data from LastPass. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Disable Multifactor](actions/disable-multifactor.md) | PUT | Disables multifactor authentication for a LastPass user. |
| [Disable User](actions/disable-user.md) | PUT | Disables an existing user in LastPass. |
| [Enable User](actions/enable-user.md) | PUT | Enables an existing user in LastPass. |
| [Reinvite User](actions/reinvite-user.md) | PUT | Reinvites an existing user in LastPass. |
| [Require Master Password Change](actions/require-master-password-change.md) | PUT | Requires a LastPass user to change their master password. |
| [Send Password Reset Email](actions/send-password-reset-email.md) | PUT | Sends a password reset email to a LastPass user. |
| [Update User Email](actions/update-user-email.md) | PUT | Updates a LastPass user's email address. |

