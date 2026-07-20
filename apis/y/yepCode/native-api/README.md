# YepCode: Native API Reference

A consolidated summary of YepCode's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html
- **OpenAPI specification:** https://cloud.yepcode.io/api/rest/public/api-docs
- **API base URL:** `https://cloud.yepcode.io/api/{team}/rest`

## Authentication

### OAuth 2.0

### Credentials

- **Team ID:** `team` · required · YepCode Team ID used in the REST API base URL, matching https://cloud.yepcode.io/{team}.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://cloud.yepcode.io/auth/realms/yepcode/protocol/openid-connect/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://yepcode.io/docs/settings/api-credentials/)

## API conventions

The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create module](actions/create-module.md) | `POST /modules` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/createModule) |
| [Create module version alias](actions/create-module-version-alias.md) | `POST /modules/:moduleId/aliases` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/createModuleVersionAlias) |
| [Create process](actions/create-process.md) | `POST /processes` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/createProcess) |
| [Create process version alias](actions/create-process-version-alias.md) | `POST /processes/:processId/aliases` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/createProcessVersionAlias) |
| [Create variable](actions/create-variable.md) | `POST /variables` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Variables/createVariable) |
| [Delete module](actions/delete-module.md) | `DELETE /modules/:id` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/deleteModule) |
| [Delete process](actions/delete-process.md) | `DELETE /processes/:identifier` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/deleteProcess) |
| [Delete variable](actions/delete-variable.md) | `DELETE /variables/:id` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Variables/deleteVariable) |
| [Execute process async](actions/execute-process-async.md) | `POST /processes/:identifier/execute` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/executeProcessAsync) |
| [Get execution](actions/get-execution.md) | `GET /executions/:id` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Executions/getExecution) |
| [Get execution logs](actions/get-execution-logs.md) | `GET /executions/:id/logs` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Executions/getExecutionLogs) |
| [Get executions](actions/get-executions.md) | `GET /executions` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Executions/getExecutions) |
| [Get module](actions/get-module.md) | `GET /modules/:id` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/getModule) |
| [Get module version alias](actions/get-module-version-alias.md) | `GET /modules/:moduleId/aliases/:aliasId` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/getModuleVersionAlias) |
| [Get module version aliases](actions/get-module-version-aliases.md) | `GET /modules/:moduleId/aliases` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/getModuleVersionAliases) |
| [Get module versions](actions/get-module-versions.md) | `GET /modules/:moduleId/versions` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/getModuleVersions) |
| [Get modules](actions/get-modules.md) | `GET /modules` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/getModules) |
| [Get process](actions/get-process.md) | `GET /processes/:identifier` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/getProcess) |
| [Get process version alias](actions/get-process-version-alias.md) | `GET /processes/:processId/aliases/:aliasId` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/getProcessVersionAlias) |
| [Get process version aliases](actions/get-process-version-aliases.md) | `GET /processes/:processId/aliases` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/getProcessVersionAliases) |
| [Get process versions](actions/get-process-versions.md) | `GET /processes/:processId/versions` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/getProcessVersions) |
| [Get processes](actions/get-processes.md) | `GET /processes` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/getProcesses) |
| [Get scheduled process](actions/get-schedule.md) | `GET /schedules/:id` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Schedules/getSchedule) |
| [Get scheduled processes](actions/get-schedules.md) | `GET /schedules` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Schedules/getSchedules) |
| [Get storage object helper](actions/get-storage-object-helper.md) | `GET /storage/objects/:filename` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Storage/getStorageObject) |
| [Get storage objects](actions/get-storage-objects.md) | `GET /storage/objects` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Storage/getStorageObjects) |
| [Get variables](actions/get-variables.md) | `GET /variables` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Variables/getVariables) |
| [Kill execution](actions/kill-execution.md) | `PUT /executions/:id/kill` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Executions/killExecution) |
| [Pause scheduled process](actions/pause-schedule.md) | `PUT /schedules/:id/pause` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Schedules/pauseSchedule) |
| [Publish module version](actions/publish-module-version.md) | `POST /modules/:moduleId/versions` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/publishModuleVersion) |
| [Publish process version](actions/publish-process-version.md) | `POST /processes/:processId/versions` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/publishProcessVersion) |
| [Rerun execution](actions/rerun-execution.md) | `POST /executions/:id/rerun` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Executions/rerunExecution) |
| [Resume scheduled process](actions/resume-schedule.md) | `PUT /schedules/:id/resume` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Schedules/resumeSchedule) |
| [Schedule process](actions/schedule-process.md) | `POST /processes/:identifier/schedule` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/createSchedule) |
| [Update variable](actions/update-variable.md) | `PATCH /variables/:id` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Variables/updateVariable) |
| [Upload storage object](actions/upload-storage-object.md) | `POST /storage/objects` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Storage/uploadStorageObject) |
| [Upload storage object raw](actions/upload-storage-object-raw.md) | `POST /storage/objects` | [docs](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Storage/uploadStorageObject) |
