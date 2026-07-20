# Process Street: Native API Reference

A consolidated summary of Process Street's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://public-api.process.st/api/v1.1/docs/index.html
- **OpenAPI specification:** https://public-api.process.st/api/v1.1/docs/docs.yaml
- **API base URL:** `https://public-api.process.st/api/v1.1`

## Authentication

### API Key

Connect with a Process Street administrator API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://www.process.st/help/docs/process-street-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `_` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 1 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve or Reject Task](actions/approve-or-reject-task.md) | `PUT /workflow-runs/:workflowRunId/approvals` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/tasks/PUT/workflow-runs/{workflowRunId}/approvals) |
| [Assign Workflow Run User](actions/assign-workflow-run-user.md) | `POST /workflow-runs/:workflowRunId/assignees/:email` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflow-runs/POST/workflow-runs/{workflowRunId}/assignees/{email}) |
| [Batch Update Form Field Values](actions/batch-update-form-field-values.md) | `POST /workflow-runs/:workflowRunId/form-fields` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/form-field-values/POST/workflow-runs/{workflowRunId}/form-fields) |
| [Create Workflow Run](actions/create-workflow-run.md) | `POST /workflow-runs` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflow-runs/POST/workflow-runs) |
| [Delete Workflow Run](actions/delete-workflow-run.md) | `DELETE /workflow-runs/:workflowRunId` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflow-runs/DELETE/workflow-runs/{workflowRunId}) |
| [Get Data Set Record](actions/get-data-set-record.md) | `GET /data-sets/:dataSetId/records/:dataSetRecordId` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/data-sets/GET/data-sets/{dataSetId}/records/{dataSetRecordId}) |
| [Get Task](actions/get-task.md) | `GET /workflow-runs/:workflowRunId/tasks/:taskId` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/tasks/GET/workflow-runs/{workflowRunId}/tasks/{taskId}) |
| [Get Workflow Run](actions/get-workflow-run.md) | `GET /workflow-runs/:workflowRunId` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflow-runs/GET/workflow-runs/{workflowRunId}) |
| [List Approvals](actions/list-approvals.md) | `GET /workflow-runs/:workflowRunId/approvals` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/tasks/GET/workflow-runs/{workflowRunId}/approvals) |
| [List Data Set Records](actions/list-data-set-records.md) | `GET /data-sets/:dataSetId/records` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/data-sets/GET/data-sets/{dataSetId}/records) |
| [List Data Sets](actions/list-data-sets.md) | `GET /data-sets` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/data-sets/GET/data-sets) |
| [List Form Field Options](actions/list-form-field-options.md) | `GET /workflows/:workflowId/form-fields/:formFieldId/options` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/form-fields/GET/workflows/{workflowId}/form-fields/{formFieldId}/options) |
| [List Form Fields](actions/list-form-fields.md) | `GET /workflows/:workflowId/form-fields` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/form-fields/GET/workflows/{workflowId}/form-fields) |
| [List Task Form Field Values](actions/list-task-form-field-values.md) | `GET /workflow-runs/:workflowRunId/tasks/:taskId/form-fields` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/form-field-values/GET/workflow-runs/{workflowRunId}/tasks/{taskId}/form-fields) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/users/GET/users) |
| [List Workflow Run Assignees](actions/list-workflow-run-assignees.md) | `GET /workflow-runs/:workflowRunId/assignees` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflow-runs/GET/workflow-runs/{workflowRunId}/assignees) |
| [List Workflow Run Form Field Values](actions/list-workflow-run-form-field-values.md) | `GET /workflow-runs/:workflowRunId/form-fields` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/form-field-values/GET/workflow-runs/{workflowRunId}/form-fields) |
| [List Workflow Run Tasks](actions/list-workflow-run-tasks.md) | `GET /workflow-runs/:workflowRunId/tasks` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/tasks/GET/workflow-runs/{workflowRunId}/tasks) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflows/GET/workflows) |
| [Search Workflow Runs](actions/search-workflow-runs.md) | `GET /workflow-runs` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflow-runs/GET/workflow-runs) |
| [Test Authentication](actions/test-authentication.md) | `GET /testAuth` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/utilities/GET/testAuth) |
| [Unassign Workflow Run User](actions/unassign-workflow-run-user.md) | `DELETE /workflow-runs/:workflowRunId/assignees/:email` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflow-runs/DELETE/workflow-runs/{workflowRunId}/assignees/{email}) |
| [Update Task](actions/update-task.md) | `PUT /workflow-runs/:workflowRunId/tasks/:taskId` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/tasks/PUT/workflow-runs/{workflowRunId}/tasks/{taskId}) |
| [Update Workflow Run](actions/update-workflow-run.md) | `PUT /workflow-runs/:workflowRunId` | [docs](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflow-runs/PUT/workflow-runs/{workflowRunId}) |
