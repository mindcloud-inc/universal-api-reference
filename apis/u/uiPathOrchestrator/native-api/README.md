# UiPath Orchestrator: Native API Reference

A consolidated summary of UiPath Orchestrator's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/introduction
- **API base URL:** `https://cloud.uipath.com/{organizationName}/{tenantName}/orchestrator_`

## Authentication

### OAuth2 Client Credentials

Connects to UiPath Orchestrator with a confidential external application using the client credentials flow.

### Credentials

- **Cloud Organization:** `organizationName` · required · The UiPath Automation Cloud organization name used in URLs, for example the value in https://cloud.uipath.com/{organizationName}/.
- **Tenant Name:** `tenantName` · required · The UiPath Orchestrator tenant name used in URLs, such as DefaultTenant.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://cloud.uipath.com/{{credentials.organizationName}}/identity_/connect/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://cloud.uipath.com/{{credentials.organizationName}}/identity_/connect/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `OR.Default`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.uipath.com/automation-cloud/automation-cloud/latest/api-guide/accessing-uipath-resources-using-external-applications)

## API conventions

Responses from this API use JSON. Response data is read from `value`.

## Pagination

Use `$top` in the query string to set the page size (default 100; accepted range 1–1000). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `ne`.

## Sorting

Set the sort field with `$orderby` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create asset](actions/create-asset.md) | `POST /odata/Assets` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/assets-requests) |
| [Create queue](actions/create-queue.md) | `POST /odata/QueueDefinitions` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/queue-items-requests) |
| [Delete asset](actions/delete-asset.md) | `DELETE /odata/Assets(:id)` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/assets-requests) |
| [Get asset](actions/get-asset.md) | `GET /odata/Assets(:id)` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/assets-requests) |
| [Get folder](actions/get-folder.md) | `GET /odata/Folders(:id)` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/folders-requests) |
| [Get job](actions/get-job.md) | `GET /odata/Jobs(:id)` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/jobs-requests) |
| [Get machine](actions/get-machine.md) | `GET /odata/Machines(:id)` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/machines-requests) |
| [Get process](actions/get-process.md) | `GET /odata/Processes(:id)` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/processes-requests) |
| [Get queue](actions/get-queue.md) | `GET /odata/QueueDefinitions(:id)` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/queue-items-requests) |
| [Get queue item](actions/get-queue-item.md) | `GET /odata/QueueItems(:id)` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/queue-items-requests) |
| [Get robot](actions/get-robot.md) | `GET /odata/Robots(:id)` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/robots-requests) |
| [Get schedule](actions/get-schedule.md) | `GET /odata/ProcessSchedules(:id)` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/schedules-requests) |
| [Get task](actions/get-task.md) | `GET /odata/Tasks(:id)` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/tasks-requests) |
| [List assets](actions/list-assets.md) | `GET /odata/Assets` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/assets-requests) |
| [List folders](actions/list-folders.md) | `GET /odata/Folders` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/folders-requests) |
| [List jobs](actions/list-jobs.md) | `GET /odata/Jobs` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/jobs-requests) |
| [List machines](actions/list-machines.md) | `GET /odata/Machines` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/machines-requests) |
| [List processes](actions/list-processes.md) | `GET /odata/Processes` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/processes-requests) |
| [List queue items](actions/list-queue-items.md) | `GET /odata/QueueItems` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/queue-items-requests) |
| [List queues](actions/list-queues.md) | `GET /odata/QueueDefinitions` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/queue-items-requests) |
| [List robots](actions/list-robots.md) | `GET /odata/Robots` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/robots-requests) |
| [List runtime licenses](actions/list-runtime-licenses.md) | `GET /odata/LicensesRuntime` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/license-requests) |
| [List schedules](actions/list-schedules.md) | `GET /odata/ProcessSchedules` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/schedules-requests) |
| [List settings](actions/list-settings.md) | `GET /odata/Settings` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/settings-requests) |
| [List tasks across folders](actions/list-tasks-across-folders.md) | `GET /odata/Tasks/UiPath.Server.Configuration.OData.GetTasksAcrossFolders` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/tasks-requests) |
| [List tenants](actions/list-tenants.md) | `GET /odata/Tenants` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/tenants-requests) |
| [List users](actions/list-users.md) | `GET /odata/Users` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/users-requests) |
| [Start jobs](actions/start-jobs.md) | `POST /odata/Jobs/UiPath.Server.Configuration.OData.StartJobs` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/jobs-requests) |
| [Stop job](actions/stop-job.md) | `POST /odata/Jobs/UiPath.Server.Configuration.OData.StopJob` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/jobs-requests) |
| [Update asset](actions/update-asset.md) | `PUT /odata/Assets(:id)` | [docs](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/assets-requests) |
