# Databricks: Native API Reference

A consolidated summary of Databricks's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.databricks.com/api/workspace/introduction
- **API base URL:** `https://accounts.cloud.databricks.com`

## Authentication

### OAuth 2.0 (Service Principal)

Authenticate with a Databricks service principal using OAuth 2.0 machine-to-machine credentials.

### Credentials

- **Workspace URL:** `host` · required · Your Databricks workspace URL, for example https://dbc-a1b2345c-d6e7.cloud.databricks.com.
- **Account ID:** `accountId` · required · Your Databricks account ID from the Databricks account console.
- **Client ID:** `clientId` · required · The Databricks service principal application ID (client ID).
- **Client Secret:** `clientSecret` · required · The OAuth secret for the Databricks service principal.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://accounts.cloud.databricks.com/oidc/accounts/{{credentials.accountId}}/v1/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `all-apis`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.databricks.com/aws/en/dev-tools/auth/oauth-m2m)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `next_page_token`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Cluster](actions/create-cluster.md) | `POST {{credentials.host}}/api/2.1/clusters/create` | [docs](https://docs.databricks.com/api/workspace/clusters/create) |
| [Create Group](actions/create-group.md) | `POST /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Groups` | [docs](https://docs.databricks.com/api/account/accountgroups/create) |
| [Create Job](actions/create-job.md) | `POST {{credentials.host}}/api/2.2/jobs/create` | [docs](https://docs.databricks.com/api/workspace/jobs/create) |
| [Create Pipeline](actions/create-pipeline.md) | `POST {{credentials.host}}/api/2.0/pipelines` | [docs](https://docs.databricks.com/api/workspace/pipelines/create) |
| [Create Service Principal](actions/create-service-principal.md) | `POST /api/2.0/accounts/{{credentials.accountId}}/scim/v2/ServicePrincipals` | [docs](https://docs.databricks.com/api/account/accountserviceprincipals/create) |
| [Create User](actions/create-user.md) | `POST /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Users` | [docs](https://docs.databricks.com/api/account/accountusers/create) |
| [Delete Cluster](actions/delete-cluster.md) | `POST {{credentials.host}}/api/2.1/clusters/delete` | [docs](https://docs.databricks.com/api/workspace/clusters/delete) |
| [Delete Workspace Assignment](actions/delete-workspace-assignment.md) | `DELETE /api/2.0/accounts/{{credentials.accountId}}/workspaces/:workspaceId/permissionassignments/principals/:principalId` | [docs](https://docs.databricks.com/api/account/workspaceassignment/delete) |
| [Get Cluster](actions/get-cluster.md) | `GET {{credentials.host}}/api/2.1/clusters/get` | [docs](https://docs.databricks.com/api/workspace/clusters/get) |
| [Get Group](actions/get-group.md) | `GET /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Groups/:groupId` | [docs](https://docs.databricks.com/api/account/accountgroups/get) |
| [Get Job](actions/get-job.md) | `GET {{credentials.host}}/api/2.2/jobs/get` | [docs](https://docs.databricks.com/api/workspace/jobs/get) |
| [Get Job Run](actions/get-job-run.md) | `GET {{credentials.host}}/api/2.2/jobs/runs/get` | [docs](https://docs.databricks.com/api/workspace/jobs/getrun) |
| [Get Job Run Output](actions/get-job-run-output.md) | `GET {{credentials.host}}/api/2.2/jobs/runs/get-output` | [docs](https://docs.databricks.com/api/workspace/jobs/getrunoutput) |
| [Get Pipeline](actions/get-pipeline.md) | `GET {{credentials.host}}/api/2.0/pipelines/:pipelineId` | [docs](https://docs.databricks.com/api/workspace/pipelines/get) |
| [Get Service Principal](actions/get-service-principal.md) | `GET /api/2.0/accounts/{{credentials.accountId}}/scim/v2/ServicePrincipals/:servicePrincipalId` | [docs](https://docs.databricks.com/api/account/accountserviceprincipals/get) |
| [Get SQL Warehouse](actions/get-sql-warehouse.md) | `GET {{credentials.host}}/api/2.0/sql/warehouses/:warehouseId` | [docs](https://docs.databricks.com/api/workspace/warehouses/get) |
| [Get User](actions/get-user.md) | `GET /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Users/:userId` | [docs](https://docs.databricks.com/api/account/accountusers/get) |
| [Get Workspace](actions/get-workspace.md) | `GET /api/2.0/accounts/{{credentials.accountId}}/workspaces/:workspaceId` | [docs](https://docs.databricks.com/api/account/workspaces/get) |
| [List Clusters](actions/list-clusters.md) | `GET {{credentials.host}}/api/2.1/clusters/list` | [docs](https://docs.databricks.com/api/workspace/clusters/list) |
| [List Groups](actions/list-groups.md) | `GET /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Groups` | [docs](https://docs.databricks.com/api/account/accountgroups/list) |
| [List Job Runs](actions/list-job-runs.md) | `GET {{credentials.host}}/api/2.2/jobs/runs/list` | [docs](https://docs.databricks.com/api/workspace/jobs/listruns) |
| [List Jobs](actions/list-jobs.md) | `GET {{credentials.host}}/api/2.2/jobs/list` | [docs](https://docs.databricks.com/api/workspace/jobs/list) |
| [List Pipelines](actions/list-pipelines.md) | `GET {{credentials.host}}/api/2.0/pipelines` | [docs](https://docs.databricks.com/api/workspace/pipelines/listpipelines) |
| [List Service Principals](actions/list-service-principals.md) | `GET /api/2.0/accounts/{{credentials.accountId}}/scim/v2/ServicePrincipals` | [docs](https://docs.databricks.com/api/account/accountserviceprincipals/list) |
| [List SQL Warehouses](actions/list-sql-warehouses.md) | `GET {{credentials.host}}/api/2.0/sql/warehouses` | [docs](https://docs.databricks.com/api/workspace/warehouses/list) |
| [List Users](actions/list-users.md) | `GET /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Users` | [docs](https://docs.databricks.com/api/account/accountusers/list) |
| [List Workspace Assignments](actions/list-workspace-assignments.md) | `GET /api/2.0/accounts/{{credentials.accountId}}/workspaces/:workspaceId/permissionassignments` | [docs](https://docs.databricks.com/api/account/workspaceassignment/get) |
| [List Workspaces](actions/list-workspaces.md) | `GET /api/2.0/accounts/{{credentials.accountId}}/workspaces` | [docs](https://docs.databricks.com/api/account/workspaces/list) |
| [Restart Cluster](actions/restart-cluster.md) | `POST {{credentials.host}}/api/2.1/clusters/restart` | [docs](https://docs.databricks.com/api/workspace/clusters/restart) |
| [Run Job Now](actions/run-job-now.md) | `POST {{credentials.host}}/api/2.2/jobs/run-now` | [docs](https://docs.databricks.com/api/workspace/jobs/runnow) |
| [Start Cluster](actions/start-cluster.md) | `POST {{credentials.host}}/api/2.1/clusters/start` | [docs](https://docs.databricks.com/api/workspace/clusters/start) |
| [Start Pipeline Update](actions/start-pipeline-update.md) | `POST {{credentials.host}}/api/2.0/pipelines/:pipelineId/updates` | [docs](https://docs.databricks.com/api/workspace/pipelines/startupdate) |
| [Start SQL Warehouse](actions/start-sql-warehouse.md) | `POST {{credentials.host}}/api/2.0/sql/warehouses/:warehouseId/start` | [docs](https://docs.databricks.com/api/workspace/warehouses/start) |
| [Update Cluster](actions/update-cluster.md) | `POST {{credentials.host}}/api/2.1/clusters/update` | [docs](https://docs.databricks.com/api/workspace/clusters/update) |
| [Update Group](actions/update-group.md) | `PATCH /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Groups/:groupId` | [docs](https://docs.databricks.com/api/account/accountgroups/patch) |
| [Update Job](actions/update-job.md) | `POST {{credentials.host}}/api/2.2/jobs/update` | [docs](https://docs.databricks.com/api/workspace/jobs/update) |
| [Update Service Principal](actions/update-service-principal.md) | `PATCH /api/2.0/accounts/{{credentials.accountId}}/scim/v2/ServicePrincipals/:servicePrincipalId` | [docs](https://docs.databricks.com/api/account/accountserviceprincipals/patch) |
| [Update User](actions/update-user.md) | `PATCH /api/2.0/accounts/{{credentials.accountId}}/scim/v2/Users/:userId` | [docs](https://docs.databricks.com/api/account/accountusers/patch) |
| [Update Workspace](actions/update-workspace.md) | `PATCH /api/2.0/accounts/{{credentials.accountId}}/workspaces/:workspaceId` | [docs](https://docs.databricks.com/api/account/workspaces/update) |
| [Update Workspace Assignment](actions/update-workspace-assignment.md) | `PUT /api/2.0/accounts/{{credentials.accountId}}/workspaces/:workspaceId/permissionassignments/principals/:principalId` | [docs](https://docs.databricks.com/api/account/workspaceassignment/update) |
