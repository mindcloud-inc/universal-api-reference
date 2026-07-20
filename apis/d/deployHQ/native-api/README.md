# DeployHQ: Native API Reference

A consolidated summary of DeployHQ's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.deployhq.com/support/api
- **OpenAPI specification:** https://api.deployhq.com/docs.json
- **API base URL:** `https://{account}.deployhq.com`

## Authentication

### Basic

Use your DeployHQ email address as the Basic Auth username and your DeployHQ API key as the password. Add your DeployHQ account subdomain so MindCloud can call the correct account URL.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Account Subdomain:** `account` · required · The DeployHQ account subdomain from https://<account>.deployhq.com/. Enter only the account segment, without .deployhq.com.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.deployhq.com/support/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `data.pagination.total_pages`. The current page number is read from `data.pagination.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `503`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Abort Deployment](actions/abort-deployment.md) | `POST /projects/:project_id/deployments/:id/abort` | [docs](https://api.deployhq.com/docs#tag/Deployments/operation/abortProjectDeployment) |
| [Create Or Replace Repository](actions/create-or-replace-repository.md) | `POST /projects/:project_id/repository` | [docs](https://api.deployhq.com/docs#tag/Repositories/operation/createProjectRepository) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://api.deployhq.com/docs#tag/Projects/operation/createProject) |
| [Create Server](actions/create-server.md) | `POST /projects/:project_id/servers` | [docs](https://api.deployhq.com/docs#tag/Servers/operation/createProjectServer) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://api.deployhq.com/docs#tag/Projects/operation/deleteProject) |
| [Delete Server](actions/delete-server.md) | `DELETE /projects/:project_id/servers/:id` | [docs](https://api.deployhq.com/docs#tag/Servers/operation/deleteProjectServer) |
| [Get Deployment](actions/get-deployment.md) | `GET /projects/:project_id/deployments/:id` | [docs](https://api.deployhq.com/docs#tag/Deployments/operation/getProjectDeploymentById) |
| [Get Latest Revision](actions/get-latest-revision.md) | `GET /projects/:project_id/repository/latest_revision` | [docs](https://api.deployhq.com/docs#tag/Repositories/operation/latestRevisionProjectRepository) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://api.deployhq.com/docs#tag/Projects/operation/getProject) |
| [Get Repository](actions/get-repository.md) | `GET /projects/:project_id/repository` | [docs](https://api.deployhq.com/docs#tag/Repositories/operation/getProjectRepository) |
| [Get Server](actions/get-server.md) | `GET /projects/:project_id/servers/:id` | [docs](https://api.deployhq.com/docs#tag/Servers/operation/getProjectServerById) |
| [List Deployments](actions/list-deployments.md) | `GET /projects/:project_id/deployments` | [docs](https://api.deployhq.com/docs#tag/Deployments/operation/listProjectDeployments) |
| [List Integrations](actions/list-integrations.md) | `GET /projects/:project_id/integrations` | [docs](https://api.deployhq.com/docs#tag/Integrations/operation/listProjectIntegrations) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://api.deployhq.com/docs#tag/Projects/operation/listProjects) |
| [List Recent Commits](actions/list-recent-commits.md) | `GET /projects/:project_id/repository/recent_commits` | [docs](https://api.deployhq.com/docs#tag/Repositories/operation/recentCommitsProjectRepository) |
| [List Repository Branches](actions/list-repository-branches.md) | `GET /projects/:project_id/repository/branches` | [docs](https://api.deployhq.com/docs#tag/Repositories/operation/branchesProjectRepository) |
| [List Servers](actions/list-servers.md) | `GET /projects/:project_id/servers` | [docs](https://api.deployhq.com/docs#tag/Servers/operation/listProjectServers) |
| [Queue Deployment](actions/queue-deployment.md) | `POST /projects/:project_id/deployments` | [docs](https://api.deployhq.com/docs#tag/Deployments/operation/createProjectDeployment) |
| [Retry Deployment](actions/retry-deployment.md) | `POST /projects/:project_id/deployments/:id/retry` | [docs](https://api.deployhq.com/docs#tag/Deployments/operation/retryProjectDeploymentRetry) |
| [Rollback Deployment](actions/rollback-deployment.md) | `POST /projects/:project_id/deployments/:id/rollback` | [docs](https://api.deployhq.com/docs#tag/Deployments/operation/rollbackProjectDeployment) |
| [Run Server Test Access](actions/run-server-test-access.md) | `POST /projects/:project_id/servers/:server_id/test_access` | [docs](https://api.deployhq.com/docs#tag/Test-Access/operation/createProjectServerTestAccess) |
| [Update Project](actions/update-project.md) | `PATCH /projects/:id` | [docs](https://api.deployhq.com/docs#tag/Projects/operation/updateProject) |
| [Update Repository](actions/update-repository.md) | `PATCH /projects/:project_id/repository` | [docs](https://api.deployhq.com/docs#tag/Repositories/operation/updateProjectRepository) |
| [Update Server](actions/update-server.md) | `PATCH /projects/:project_id/servers/:id` | [docs](https://api.deployhq.com/docs#tag/Servers/operation/updateProjectServer) |
