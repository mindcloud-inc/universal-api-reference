# Skyvern: Native API Reference

A consolidated summary of Skyvern's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://www.skyvern.com/docs/api-reference
- **OpenAPI specification:** https://api.skyvern.com/openapi.json
- **API base URL:** `https://api.skyvern.com`

## Authentication

### API Key

Connect to Skyvern with an API key from Skyvern Cloud.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://www.skyvern.com/docs/getting-started/quickstart/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Run](actions/cancel-run.md) | `POST /v1/runs/:run_id/cancel` | [docs](https://www.skyvern.com/docs/api-reference/agent/cancel-a-run-by-id) |
| [Create Folder](actions/create-folder.md) | `POST /v1/folders` | [docs](https://www.skyvern.com/docs/api-reference/workflows) |
| [Create Script](actions/create-script.md) | `POST /v1/scripts` | [docs](https://www.skyvern.com/docs/api-reference/scripts/create-script) |
| [Create Workflow](actions/create-workflow.md) | `POST /v1/workflows` | [docs](https://www.skyvern.com/docs/api-reference/workflows/create-a-new-workflow) |
| [Delete Workflow](actions/delete-workflow.md) | `POST /v1/workflows/:workflow_id/delete` | [docs](https://www.skyvern.com/docs/api-reference/workflows/delete-a-workflow) |
| [Get Artifact](actions/get-artifact.md) | `GET /v1/artifacts/:artifact_id` | [docs](https://www.skyvern.com/docs/api-reference/artifacts/get-an-artifact) |
| [Get Run](actions/get-run.md) | `GET /v1/runs/:run_id` | [docs](https://www.skyvern.com/docs/api-reference/agent/get-a-run-by-id) |
| [Get Run Timeline](actions/get-run-timeline.md) | `GET /v1/runs/:run_id/timeline` | [docs](https://www.skyvern.com/docs/api-reference/agent/get-run-timeline) |
| [Get Script](actions/get-script.md) | `GET /v1/scripts/:script_id` | [docs](https://www.skyvern.com/docs/api-reference/scripts/get-script-by-id) |
| [Get Workflow](actions/get-workflow.md) | `GET /v1/workflows/:workflow_permanent_id` | [docs](https://www.skyvern.com/docs/api-reference/workflows) |
| [List Folders](actions/list-folders.md) | `GET /v1/folders` | [docs](https://www.skyvern.com/docs/api-reference/workflows) |
| [List Run Artifacts](actions/list-run-artifacts.md) | `GET /v1/runs/:run_id/artifacts` | [docs](https://www.skyvern.com/docs/api-reference/artifacts/get-artifacts-for-a-run) |
| [List Workflow Runs](actions/list-workflow-runs.md) | `GET /v1/workflows/runs` | [docs](https://www.skyvern.com/docs/api-reference/workflows) |
| [List Workflow Versions](actions/list-workflow-versions.md) | `GET /v1/workflows/:workflow_permanent_id/versions` | [docs](https://www.skyvern.com/docs/api-reference/workflows) |
| [List Workflows](actions/list-workflows.md) | `GET /v1/workflows` | [docs](https://www.skyvern.com/docs/api-reference/workflows/get-workflows) |
| [Retry Run Webhook](actions/retry-run-webhook.md) | `POST /v1/runs/:run_id/retry_webhook` | [docs](https://www.skyvern.com/docs/api-reference/agent/retry-run-webhook) |
| [Run File Download Task](actions/run-file-download-task.md) | `POST /v1/run/tasks/download_files` | [docs](https://www.skyvern.com/docs/api-reference/agent/file-download-task) |
| [Run Login Task](actions/run-login-task.md) | `POST /v1/run/tasks/login` | [docs](https://www.skyvern.com/docs/api-reference/agent/login-task) |
| [Run Task](actions/run-task.md) | `POST /v1/run/tasks` | [docs](https://www.skyvern.com/docs/api-reference/agent/run-a-task) |
| [Run Workflow](actions/run-workflow.md) | `POST /v1/run/workflows` | [docs](https://www.skyvern.com/docs/api-reference/workflows/run-a-workflow) |
| [Update Workflow](actions/update-workflow.md) | `POST /v1/workflows/:workflow_id` | [docs](https://www.skyvern.com/docs/api-reference/workflows/update-a-workflow) |
| [Update Workflow Folder](actions/update-workflow-folder.md) | `PUT /v1/workflows/:workflow_permanent_id/folder` | [docs](https://www.skyvern.com/docs/api-reference/workflows) |
