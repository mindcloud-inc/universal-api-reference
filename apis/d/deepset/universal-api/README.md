# <img src="https://images.mindcloud.co/apps/icons/51827949_1776944418213.png" alt="Deepset logo" width="28" height="28"> Deepset: Universal API

Build production-grade retrieval, search, pipeline, workspace, job, feedback, and administration automations for deepset Haystack Enterprise Platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deepset/latest
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.deepset.ai/
- **Vendor API docs:** https://docs.cloud.deepset.ai/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Read Current User](actions/read-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/read-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline Logs](actions/get-pipeline-logs.md) | GET | Retrieves logs for a Deepset pipeline. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Get Index By Name](actions/get-index-by-name.md) | GET | Retrieves a Deepset index by name. |
| [List Indexes](actions/list-indexes.md) | GET | Retrieves indexes from a Deepset workspace. |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Get Query Set](actions/get-query-set.md) | GET | Retrieves a query set from a Deepset workspace. |
| [Get Query Sets](actions/get-query-sets.md) | GET | Retrieves query sets from a Deepset workspace. |
| [List Datasets](actions/list-datasets.md) | GET | Retrieves datasets from a Deepset workspace. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from a Deepset index. |
| [Get Pipeline Visualization](actions/get-pipeline-visualization.md) | GET | Retrieves visualization data for a Deepset pipeline. |
| [Get Pipeline YAML Configs](actions/get-pipeline-yaml-configs.md) | GET | Retrieves YAML configuration for a Deepset pipeline. |
| [Query Documents](actions/query-documents.md) | GET | Queries documents in a Deepset index. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET | Retrieves a file from a Deepset workspace. |
| [Get File Metadata](actions/get-file-metadata.md) | GET | Retrieves metadata for a file in Deepset. |
| [List Files](actions/list-files.md) | GET | Retrieves files from a Deepset workspace. |
| [Query Files](actions/query-files.md) | GET | Queries files in a Deepset workspace with SQL. |

### Issues

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline Issues](actions/get-pipeline-issues.md) | GET | Retrieves issues for a Deepset pipeline. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from a Deepset workspace. |
| [Get Jobs](actions/get-jobs.md) | GET | Retrieves jobs from a Deepset workspace. |
| [Get Shared Job](actions/get-shared-job.md) | GET | Retrieves a shared job from a Deepset workspace. |
| [Get Shared Jobs](actions/get-shared-jobs.md) | GET | Retrieves shared jobs from a Deepset workspace. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Chat](actions/chat.md) | GET | Chats with a Deepset pipeline using one or more queries. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Count Documents](actions/count-documents.md) | GET | Retrieves the document count for a Deepset index. |
| [Get Pipeline Stats](actions/get-pipeline-stats.md) | GET | Retrieves statistics for a Deepset pipeline. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves your current Deepset organization details. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [Get Permissions](actions/get-permissions.md) | GET | Retrieves permissions for your Deepset organization. |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [Get Pipeline](actions/get-pipeline.md) | GET | Retrieves a Deepset pipeline by name. |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from a Deepset workspace. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Search Pipeline](actions/search-pipeline.md) | GET | Searches a Deepset pipeline with one or more queries. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Get Roles](actions/get-roles.md) | GET | Retrieves roles for a Deepset organization. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Sessions](actions/get-search-sessions.md) | GET | Retrieves search sessions from a Deepset workspace. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Health](actions/health.md) | GET | Checks the health of the Deepset service. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a Deepset user by ID. |
| [Get Users](actions/get-users.md) | GET | Retrieves users from your Deepset organization. |
| [Read Current User](actions/read-current-user.md) | GET | Retrieves the current user from Deepset. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace By Name](actions/get-workspace-by-name.md) | GET | Retrieves a Deepset workspace by name. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from your Deepset organization. |

