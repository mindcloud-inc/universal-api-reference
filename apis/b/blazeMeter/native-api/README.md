# BlazeMeter: Native API Reference

A consolidated summary of BlazeMeter's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://help.blazemeter.com/apidocs/
- **OpenAPI specification:** https://a.blazemeter.com/api/v4/explorer/swagger.json
- **API base URL:** `https://a.blazemeter.com/api/v4`

## Authentication

### Basic Auth

Use your BlazeMeter API key as the username and the API key secret as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Account ID:** `accountId` · required · BlazeMeter account ID for tenant-scoped endpoints.
- **Workspace ID:** `workspaceId` · required · BlazeMeter workspace ID for workspace-scoped endpoints.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://help.blazemeter.com/docs/guide/api-blazemeter-rest-apis.html)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–1000). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://help.blazemeter.com/apidocs/#tag/projects/operation/projectsCreateProject) |
| [Create User API Key](actions/create-user-api-key.md) | `POST /user/api-keys` | [docs](https://help.blazemeter.com/apidocs/#tag/user/operation/apiKeysCreateApiKey) |
| [Create Workspace Tag](actions/create-workspace-tag.md) | `POST /workspaces/:workspaceId/tags` | [docs](https://help.blazemeter.com/apidocs/#tag/workspaces/operation/tagsCreateTag) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:projectId` | [docs](https://help.blazemeter.com/apidocs/#tag/projects/operation/projectsRemoveProject) |
| [Delete User API Key](actions/delete-user-api-key.md) | `DELETE /user/api-keys/:apiKeyId` | [docs](https://help.blazemeter.com/apidocs/#tag/User-API-Keys) |
| [Delete Workspace Tag](actions/delete-workspace-tag.md) | `DELETE /workspaces/:workspaceId/tags/:tagId` | [docs](https://help.blazemeter.com/apidocs/#tag/workspaces/operation/tagsRemoveTag) |
| [Get Account](actions/get-account.md) | `GET /accounts/:accountId` | [docs](https://help.blazemeter.com/apidocs/#tag/accounts/operation/accountsRetrieveAccount) |
| [Get Account Functionalities](actions/get-account-functionalities.md) | `GET /accounts/:accountId/functionalities` | [docs](https://help.blazemeter.com/apidocs/#tag/accounts/operation/accountsRetrieveFunctionalities) |
| [Get Active Account Sessions Count](actions/get-active-account-sessions-count.md) | `GET /accounts/:accountId/sessions/active/count` | [docs](https://help.blazemeter.com/apidocs/#tag/accounts/operation/accountsRetrieveActiveSessionsCount) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://help.blazemeter.com/apidocs/#tag/user/operation/listUser) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectId` | [docs](https://help.blazemeter.com/apidocs/#tag/projects/operation/projectsRetrieveProject) |
| [Get User API Key](actions/get-user-api-key.md) | `GET /user/api-keys/:apiKeyId` | [docs](https://help.blazemeter.com/apidocs/#tag/user/operation/apiKeysRetrieveApiKey) |
| [Get User Preferences](actions/get-user-preferences.md) | `GET /user/preferences` | [docs](https://help.blazemeter.com/apidocs/#tag/user/operation/userPreferencesRetrieveUserPreferences) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/:workspaceId` | [docs](https://help.blazemeter.com/apidocs/#tag/workspaces/operation/workspacesRetrieveWorkspace) |
| [Get Workspace Active Masters Count](actions/get-workspace-active-masters-count.md) | `GET /workspaces/:workspaceId/masters/active/count` | [docs](https://help.blazemeter.com/apidocs/#tag/workspaces/operation/workspacesRetrieveActiveMastersCount) |
| [Get Workspace Active Usage](actions/get-workspace-active-usage.md) | `GET /workspaces/:workspaceId/active` | [docs](https://help.blazemeter.com/apidocs/#tag/workspaces/operation/workspacesRetrieveActiveTestsInfo) |
| [List Account Invitations](actions/list-account-invitations.md) | `GET /accounts/:accountId/invitations` | [docs](https://help.blazemeter.com/apidocs/#tag/accounts/operation/accountsRetrieveInvitationsList) |
| [List Account Invoices](actions/list-account-invoices.md) | `GET /accounts/:accountId/invoices` | [docs](https://help.blazemeter.com/apidocs/#tag/accounts/operation/accountsRetrieveInvoices) |
| [List Account Roles](actions/list-account-roles.md) | `GET /accounts/:entityId/roles` | [docs](https://help.blazemeter.com/apidocs/#tag/accounts/operation/accountsRetrieveAvailableRoles) |
| [List Account Subscriptions](actions/list-account-subscriptions.md) | `GET /accounts/:accountId/subscriptions` | [docs](https://help.blazemeter.com/apidocs/#tag/accounts/operation/accountsRetrieveSubscriptions) |
| [List Account Users](actions/list-account-users.md) | `GET /accounts/:entityId/users` | [docs](https://help.blazemeter.com/apidocs/#tag/accounts/operation/accountsRetrieveUsersList) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://help.blazemeter.com/apidocs/#tag/accounts/operation/listAccounts) |
| [List Masters](actions/list-masters.md) | `GET /masters` | [docs](https://help.blazemeter.com/apidocs/#tag/masters/operation/listMasters) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://help.blazemeter.com/apidocs/#tag/projects/operation/projectsRetrieveListOfProjects) |
| [List Tests](actions/list-tests.md) | `GET /tests` | [docs](https://help.blazemeter.com/apidocs/#tag/tests/operation/listTests) |
| [List User API Keys](actions/list-user-api-keys.md) | `GET /user/api-keys` | [docs](https://help.blazemeter.com/apidocs/#tag/user/operation/listApiKeys) |
| [List User Projects](actions/list-user-projects.md) | `GET /user/projects` | [docs](https://help.blazemeter.com/apidocs/#tag/user/operation/userRetrieveProjects) |
| [List Workspace Roles](actions/list-workspace-roles.md) | `GET /workspaces/:entityId/roles` | [docs](https://help.blazemeter.com/apidocs/#tag/workspaces/operation/workspacesRetrieveAvailableRoles) |
| [List Workspace Tags](actions/list-workspace-tags.md) | `GET /workspaces/:workspaceId/tags` | [docs](https://help.blazemeter.com/apidocs/#tag/workspaces/operation/tagsRetrieveAllTags) |
| [List Workspace Users](actions/list-workspace-users.md) | `GET /workspaces/:entityId/users` | [docs](https://help.blazemeter.com/apidocs/#tag/workspaces/operation/workspacesRetrieveUsersList) |
| [Regenerate User API Key Secret](actions/regenerate-user-api-key-secret.md) | `POST /user/api-keys/:apiKeyId/regenerate` | [docs](https://help.blazemeter.com/apidocs/#tag/user/operation/apiKeysRegenerateSecret) |
| [Update Project](actions/update-project.md) | `PUT /projects/:projectId` | [docs](https://help.blazemeter.com/apidocs/#tag/projects/operation/projectsUpdateProject) |
| [Update User API Key](actions/update-user-api-key.md) | `PUT /user/api-keys/:apiKeyId` | [docs](https://help.blazemeter.com/apidocs/#tag/user/operation/apiKeysUpdateApiKey) |
| [Update Workspace Tag](actions/update-workspace-tag.md) | `PUT /workspaces/:workspaceId/tags/:tagId` | [docs](https://help.blazemeter.com/apidocs/#tag/workspaces/operation/tagsUpdateTag) |
