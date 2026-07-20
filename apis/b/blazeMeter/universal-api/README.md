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
| [Get Account](actions/get-account.md) | GET |  |
| [Get Account Functionalities](actions/get-account-functionalities.md) | GET |  |
| [List Accounts](actions/list-accounts.md) | GET |  |

### Account Session

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Account Sessions Count](actions/get-active-account-sessions-count.md) | GET |  |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [List Account Invitations](actions/list-account-invitations.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Account Invoices](actions/list-account-invoices.md) | GET |  |

### Master

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Active Masters Count](actions/get-workspace-active-masters-count.md) | GET |  |
| [List Masters](actions/list-masters.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Delete Project](actions/delete-project.md) | DELETE |  |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [List User Projects](actions/list-user-projects.md) | GET |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Roles](actions/list-workspace-roles.md) | GET |  |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Account Roles](actions/list-account-roles.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Account Subscriptions](actions/list-account-subscriptions.md) | GET |  |

### Test

| Action | Method | Description |
| --- | --- | --- |
| [List Tests](actions/list-tests.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [List Workspace Users](actions/list-workspace-users.md) | GET |  |

### User Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create User API Key](actions/create-user-api-key.md) | POST |  |
| [Delete User API Key](actions/delete-user-api-key.md) | DELETE |  |
| [Get User API Key](actions/get-user-api-key.md) | GET |  |
| [List User API Keys](actions/list-user-api-keys.md) | GET |  |
| [Regenerate User API Key Secret](actions/regenerate-user-api-key-secret.md) | PUT |  |
| [Update User API Key](actions/update-user-api-key.md) | PUT |  |

### User Preference

| Action | Method | Description |
| --- | --- | --- |
| [Get User Preferences](actions/get-user-preferences.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Account Users](actions/list-account-users.md) | GET |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET |  |
| [Get Workspace Active Usage](actions/get-workspace-active-usage.md) | GET |  |

### Workspace Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace Tag](actions/create-workspace-tag.md) | POST |  |
| [Delete Workspace Tag](actions/delete-workspace-tag.md) | DELETE |  |
| [List Workspace Tags](actions/list-workspace-tags.md) | GET |  |
| [Update Workspace Tag](actions/update-workspace-tag.md) | PUT |  |

