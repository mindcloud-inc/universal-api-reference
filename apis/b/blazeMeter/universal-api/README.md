# <img src="https://images.mindcloud.co/apps/icons/favicon-help-blazemeter-com-48x48_1776283921057.png" alt="BlazeMeter logo" width="28" height="28"> BlazeMeter: Universal API

BlazeMeter is a performance testing platform for load, functional, API, and continuous testing workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/blazeMeter/latest
- **Category:** IT Operations / Observability
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.blazemeter.com
- **Vendor API docs:** https://help.blazemeter.com/apidocs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blazeMeter/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from BlazeMeter. |
| [Get Account Functionalities](actions/get-account-functionalities.md) | GET | Retrieves account functionalities from BlazeMeter. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from BlazeMeter. |

### Account Session

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Account Sessions Count](actions/get-active-account-sessions-count.md) | GET | Retrieves the active session count for a BlazeMeter account. |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [List Account Invitations](actions/list-account-invitations.md) | GET | Retrieves account invitations from BlazeMeter. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Account Invoices](actions/list-account-invoices.md) | GET | Retrieves account invoices from BlazeMeter. |

### Master

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Active Masters Count](actions/get-workspace-active-masters-count.md) | GET | Retrieves the active master count for a BlazeMeter workspace. |
| [List Masters](actions/list-masters.md) | GET | Retrieves masters from BlazeMeter. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a project in BlazeMeter. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes a project from BlazeMeter. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from BlazeMeter. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from BlazeMeter. |
| [List User Projects](actions/list-user-projects.md) | GET | Retrieves the current user's projects from BlazeMeter. |
| [Update Project](actions/update-project.md) | PUT | Updates a project in BlazeMeter. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Roles](actions/list-workspace-roles.md) | GET | Retrieves available workspace roles from BlazeMeter. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Account Roles](actions/list-account-roles.md) | GET | Retrieves available account roles from BlazeMeter. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Account Subscriptions](actions/list-account-subscriptions.md) | GET | Retrieves account subscriptions from BlazeMeter. |

### Test

| Action | Method | Description |
| --- | --- | --- |
| [List Tests](actions/list-tests.md) | GET | Retrieves tests from BlazeMeter. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves current user details from BlazeMeter. |
| [List Workspace Users](actions/list-workspace-users.md) | GET | Retrieves workspace users from BlazeMeter. |

### User Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create User API Key](actions/create-user-api-key.md) | POST | Creates a user API key in BlazeMeter. |
| [Delete User API Key](actions/delete-user-api-key.md) | DELETE | Deletes a user API key from BlazeMeter. |
| [Get User API Key](actions/get-user-api-key.md) | GET | Retrieves a user API key from BlazeMeter. |
| [List User API Keys](actions/list-user-api-keys.md) | GET | Retrieves user API keys from BlazeMeter. |
| [Regenerate User API Key Secret](actions/regenerate-user-api-key-secret.md) | PUT | Regenerates a user API key secret in BlazeMeter. |
| [Update User API Key](actions/update-user-api-key.md) | PUT | Updates a user API key in BlazeMeter. |

### User Preference

| Action | Method | Description |
| --- | --- | --- |
| [Get User Preferences](actions/get-user-preferences.md) | GET | Retrieves user preferences from BlazeMeter. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Account Users](actions/list-account-users.md) | GET | Retrieves account users from BlazeMeter. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from BlazeMeter. |
| [Get Workspace Active Usage](actions/get-workspace-active-usage.md) | GET | Retrieves active test usage for a BlazeMeter workspace. |

### Workspace Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace Tag](actions/create-workspace-tag.md) | POST | Creates a workspace tag in BlazeMeter. |
| [Delete Workspace Tag](actions/delete-workspace-tag.md) | DELETE | Deletes a workspace tag from BlazeMeter. |
| [List Workspace Tags](actions/list-workspace-tags.md) | GET | Retrieves workspace tags from BlazeMeter. |
| [Update Workspace Tag](actions/update-workspace-tag.md) | PUT | Updates a workspace tag in BlazeMeter. |

