# BrowserAct: Native API Reference

A consolidated summary of BrowserAct's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://docs.browseract.com/api-reference
- **API base URL:** `https://api.browseract.com/v2/workflow`

## Authentication

### API Key

Authenticate BrowserAct API requests with a BrowserAct API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.browseract.com/help/integrations--apis/api-keys--authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `items`. The total page count is read from `totalPages`. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 1; accepted range 1–500). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Running Task](actions/cancel-running-task.md) | `PUT /stop-task` | [docs](https://docs.browseract.com/api-reference/tasks/cancel-a-running-task) |
| [List Official Workflow Templates](actions/list-official-workflow-templates.md) | `GET /list-official-workflow-templates` | [docs](https://docs.browseract.com/api-reference/workflow-templates/list-official-workflow-templates) |
| [List Supported Proxy Regions](actions/list-supported-proxy-regions.md) | `GET /get-region-list` | [docs](https://docs.browseract.com/api-reference/regions/list-supported-proxy-regions) |
| [List Tasks](actions/list-tasks.md) | `GET /list-tasks` | [docs](https://docs.browseract.com/api-reference/tasks/list-tasks) |
| [List Workflows](actions/list-workflows.md) | `GET /list-workflows` | [docs](https://docs.browseract.com/api-reference/workflows/list-workflows) |
| [Resume Paused Task](actions/resume-paused-task.md) | `PUT /resume-task` | [docs](https://docs.browseract.com/api-reference/tasks/resume-a-paused-task) |
| [Retrieve Official Workflow Template](actions/retrieve-official-workflow-template.md) | `GET /get-official-workflow-template` | [docs](https://docs.browseract.com/api-reference/workflow-templates/retrieve-an-official-workflow-template) |
| [Retrieve Task](actions/retrieve-task.md) | `GET /get-task` | [docs](https://docs.browseract.com/api-reference/tasks/retrieve-a-task) |
| [Retrieve Task Status](actions/retrieve-task-status.md) | `GET /get-task-status` | [docs](https://docs.browseract.com/api-reference/tasks/retrieve-a-task-status) |
| [Retrieve Workflow](actions/retrieve-workflow.md) | `GET /get-workflow` | [docs](https://docs.browseract.com/api-reference/workflows/retrieve-a-workflow) |
| [Run Official Workflow Template](actions/run-official-workflow-template.md) | `POST /run-task-by-template` | [docs](https://docs.browseract.com/api-reference/tasks/run-an-official-workflow-template-create-a-task) |
| [Run Workflow](actions/run-workflow.md) | `POST /run-task` | [docs](https://docs.browseract.com/api-reference/tasks/run-a-workflow-create-a-task) |
