# <img src="https://images.mindcloud.co/apps/icons/images-2_1773939622911.png" alt="Databricks logo" width="28" height="28"> Databricks: Universal API

Manage Databricks account and workspace resources through official Databricks REST APIs using OAuth 2.0 service-principal credentials.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/databricks/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.databricks.com/
- **Vendor API docs:** https://docs.databricks.com/api/workspace/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/databricks/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Cluster

| Action | Method | Description |
| --- | --- | --- |
| [Create Cluster](actions/create-cluster.md) | POST | Creates a new cluster in the Databricks workspace. |
| [Delete Cluster](actions/delete-cluster.md) | DELETE | Deletes an existing cluster from the Databricks workspace. |
| [Get Cluster](actions/get-cluster.md) | GET | Retrieves a cluster from the Databricks workspace. |
| [List Clusters](actions/list-clusters.md) | GET | Retrieves clusters from the Databricks workspace. |
| [Restart Cluster](actions/restart-cluster.md) | PUT | Restarts an existing cluster in the Databricks workspace. |
| [Start Cluster](actions/start-cluster.md) | PUT | Starts an existing cluster in the Databricks workspace. |
| [Update Cluster](actions/update-cluster.md) | PUT | Updates an existing cluster in the Databricks workspace. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in the Databricks account. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from the Databricks account. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from the Databricks account. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in the Databricks account. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST | Creates a new job in the Databricks workspace. |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from the Databricks workspace. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from the Databricks workspace. |
| [Update Job](actions/update-job.md) | PUT | Updates an existing job in the Databricks workspace. |

### Job Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Run](actions/get-job-run.md) | GET | Retrieves a job run from the Databricks workspace. |
| [Get Job Run Output](actions/get-job-run-output.md) | GET | Retrieves output for a Databricks job run. |
| [List Job Runs](actions/list-job-runs.md) | GET | Retrieves job runs from the Databricks workspace. |
| [Run Job Now](actions/run-job-now.md) | POST | Runs a Databricks job immediately by job ID. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [Create Pipeline](actions/create-pipeline.md) | POST | Creates a new pipeline in the Databricks workspace. |
| [Get Pipeline](actions/get-pipeline.md) | GET | Retrieves a pipeline from the Databricks workspace. |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from the Databricks workspace. |

### Pipeline Update

| Action | Method | Description |
| --- | --- | --- |
| [Start Pipeline Update](actions/start-pipeline-update.md) | POST | Starts a pipeline update in Databricks. |

### Service Principal

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Principal](actions/create-service-principal.md) | POST | Creates a new service principal in the Databricks account. |
| [Get Service Principal](actions/get-service-principal.md) | GET | Retrieves a service principal from the Databricks account. |
| [List Service Principals](actions/list-service-principals.md) | GET | Retrieves service principals from the Databricks account. |
| [Update Service Principal](actions/update-service-principal.md) | PUT | Updates an existing service principal in the Databricks account. |

### Sql Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [Get SQL Warehouse](actions/get-sql-warehouse.md) | GET | Retrieves a SQL warehouse from the Databricks workspace. |
| [List SQL Warehouses](actions/list-sql-warehouses.md) | GET | Retrieves SQL warehouses from the Databricks workspace. |
| [Start SQL Warehouse](actions/start-sql-warehouse.md) | PUT | Starts a SQL warehouse in the Databricks workspace. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in the Databricks account. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from the Databricks account. |
| [List Users](actions/list-users.md) | GET | Retrieves users from the Databricks account. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in the Databricks account. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from the Databricks account. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from the Databricks account. |
| [Update Workspace](actions/update-workspace.md) | PUT | Updates an existing workspace in the Databricks account. |

### Workspace Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Workspace Assignment](actions/delete-workspace-assignment.md) | DELETE | Deletes a workspace assignment from Databricks. |
| [List Workspace Assignments](actions/list-workspace-assignments.md) | GET | Retrieves workspace assignments from Databricks for a workspace. |
| [Update Workspace Assignment](actions/update-workspace-assignment.md) | POST | Updates a workspace assignment in Databricks. |

