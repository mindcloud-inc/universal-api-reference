# Intradesk: Native API Reference

A consolidated summary of Intradesk's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://intradesk.ru/api/
- **OpenAPI specification:** https://bv.intradesk.ru/public/1230
- **API base URL:** `https://apigw.intradesk.ru`

## Authentication

### Bearer Access Token

Connect Intradesk using a bearer access token. Intradesk documents access-token auth through the token endpoint and supports refresh-token-capable scopes via offline_access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.intradesk.ru/connect/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.intradesk.ru/connect/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid profile email custom.profile api offline_access`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.intradesk.ru/connect/token.

[Official authentication documentation](https://intradesk.ru/api/43/)

## API conventions

Responses from this API use JSON.

## Pagination

Use `$top` in the query string to set the page size (default 25; accepted range 1–100). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `gt`, `gte`, `lt`, `lte`.

## Sorting

Set the sort field with `$orderby` in the query string. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Task](actions/archive-task.md) | `DELETE /changes/v3/Tasks` | [docs](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Tasks/delete_v3_Tasks) |
| [Copy Task](actions/copy-task.md) | `POST /changes/v1/Tasks/Copy` | [docs](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Tasks/post_v1_Tasks_Copy) |
| [Create Tag](actions/create-tag.md) | `POST /changes/v1/Tag` | [docs](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Tag/post_v1_Tag) |
| [Create Task](actions/create-task.md) | `POST /changes/v3/Tasks` | [docs](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Tasks/post_v3_Tasks) |
| [Create Task Relation](actions/create-task-relation.md) | `POST /changes/v1/TaskRelations` | [docs](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/TaskRelations/post_v1_TaskRelations) |
| [Evaluate Task](actions/evaluate-task.md) | `POST /changes/v3/Tasks/evaluate` | [docs](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Tasks/post_v3_Tasks_evaluate) |
| [Get Asset](actions/get-asset.md) | `GET /settings/api/v1/Assets/{id}` | [docs](https://apigw.intradesk.ru/settings_docs/swagger/index.html#/Assets/get_api_v1_Assets__id_) |
| [Get Client](actions/get-client.md) | `GET /settings/api/v1/clients/{id}` | [docs](https://apigw.intradesk.ru/settings_docs/swagger/index.html#/Clients/get_api_v1_clients__id_) |
| [Get Employee](actions/get-employee.md) | `GET /settings/api/v1/Employees/{id}` | [docs](https://apigw.intradesk.ru/settings_docs/swagger/index.html#/Employees/get_api_v1_Employees__id_) |
| [Get Knowledge Base Article](actions/get-knowledge-base-article.md) | `GET /knowledgebase/api/v1/Kb/{id}` | [docs](https://apigw.intradesk.ru/knowledgebase_docs/swagger/index.html#/Kb/get_api_v1_Kb__id_) |
| [Get Task History Comment](actions/get-task-history-comment.md) | `GET /taskhistory/api/v3/Lifetime/{taskId}/{historyUid}/comment` | [docs](https://apigw.intradesk.ru/taskhistory_docs/swagger/index.html#/Lifetime/get_api_v3_Lifetime__taskId___historyUid__comment) |
| [Get Task Type Fields](actions/get-task-type-fields.md) | `GET /taskform/api/TaskTypes/{ids}/fields` | [docs](https://apigw.intradesk.ru/taskform_docs/swagger/index.html#/TaskTypes/get_api_TaskTypes__ids__fields) |
| [Get User Settings](actions/get-user-settings.md) | `GET /users/api/v1/UserSettings` | [docs](https://apigw.intradesk.ru/users_docs/swagger/index.html#/UserSettings/get_api_v1_UserSettings) |
| [List Accessible Services](actions/list-accessible-services.md) | `GET /changes/api/Services` | [docs](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Services/get_api_Services) |
| [List Asset Services](actions/list-asset-services.md) | `GET /changes/api/Services/WithAssetsOnly` | [docs](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Services/get_api_Services_WithAssetsOnly) |
| [List Assets](actions/list-assets.md) | `GET /settings/odata/v1/Assets` | [docs](https://apigw.intradesk.ru/settings_docs/swagger/index.html#/Assets/get_odata_v1_Assets) |
| [List Clients](actions/list-clients.md) | `GET /settings/odata/v2/Clients` | [docs](https://apigw.intradesk.ru/settings_docs/swagger/index.html#/Clients/get_odata_v2_Clients) |
| [List Dashboard Tickets](actions/list-dashboard-tickets.md) | `GET /tasklist/odata/Dashboard` | [docs](https://apigw.intradesk.ru/tasklist_docs/swagger/index.html#/Dashboard/get_odata_Dashboard) |
| [List Employees](actions/list-employees.md) | `GET /settings/odata/v2/Employees` | [docs](https://apigw.intradesk.ru/settings_docs/swagger/index.html#/Employees/get_odata_v2_Employees) |
| [List Knowledge Base Articles](actions/list-knowledge-base-articles.md) | `GET /knowledgebase/odata/v1/Kb` | [docs](https://apigw.intradesk.ru/knowledgebase_docs/swagger/index.html#/Kb/get_odata_v1_Kb) |
| [List Priorities](actions/list-priorities.md) | `GET /taskform/api/Priorities` | [docs](https://apigw.intradesk.ru/taskform_docs/swagger/index.html#/Priorities/get_api_Priorities) |
| [List Tags](actions/list-tags.md) | `GET /taskform/api/Tags` | [docs](https://apigw.intradesk.ru/taskform_docs/swagger/index.html#/Tags/get_api_Tags) |
| [List Task Expenses](actions/list-task-expenses.md) | `GET /taskform/api/v2/TaskExpense/{taskNumber}` | [docs](https://apigw.intradesk.ru/taskform_docs/swagger/index.html#/TaskExpense/get_api_v2_TaskExpense__taskNumber_) |
| [List Task History](actions/list-task-history.md) | `GET /taskhistory/api/v3/Lifetime/{taskid}/full` | [docs](https://apigw.intradesk.ru/taskhistory_docs/swagger/index.html#/Lifetime/get_api_v3_Lifetime__taskid__full) |
| [List Task Inventory](actions/list-task-inventory.md) | `GET /taskform/api/TaskInventory/{taskId}` | [docs](https://apigw.intradesk.ru/taskform_docs/swagger/index.html#/TaskInventory/get_api_TaskInventory__taskId_) |
| [List Task Relations](actions/list-task-relations.md) | `GET /taskform/api/TaskRelations/{taskNumber}` | [docs](https://apigw.intradesk.ru/taskform_docs/swagger/index.html#/TaskRelations/get_api_TaskRelations__taskNumber_) |
| [List Task Statuses](actions/list-task-statuses.md) | `GET /taskform/api/Statuses` | [docs](https://apigw.intradesk.ru/taskform_docs/swagger/index.html#/Statuses/get_api_Statuses) |
| [List Task Types](actions/list-task-types.md) | `GET /taskform/api/TaskTypes` | [docs](https://apigw.intradesk.ru/taskform_docs/swagger/index.html#/TaskTypes/get_api_TaskTypes) |
| [List Tasks](actions/list-tasks.md) | `GET /tasklist/odata/v3/Tasks` | [docs](https://apigw.intradesk.ru/tasklist_docs/swagger/index.html#/Tasks/get_odata_v3_Tasks) |
| [List Workflow Statuses](actions/list-workflow-statuses.md) | `GET /taskform/api/Workflows/{id}/statuses` | [docs](https://apigw.intradesk.ru/taskform_docs/swagger/index.html#/Workflows/get_api_Workflows__id__statuses) |
| [List Workflow Transition Statuses](actions/list-workflow-transition-statuses.md) | `GET /changes/api/Rules/transitionstatuses/{workflowId}` | [docs](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Rules/get_api_Rules_transitionstatuses__workflowId_) |
| [List Workflows](actions/list-workflows.md) | `GET /taskform/api/Workflows` | [docs](https://apigw.intradesk.ru/taskform_docs/swagger/index.html#/Workflows/get_api_Workflows) |
| [Log Task Expense](actions/log-task-expense.md) | `PUT /changes/v1/TaskExpenses` | [docs](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/TaskExpenses/put_v1_TaskExpenses) |
| [Log Task Inventory](actions/log-task-inventory.md) | `PUT /changes/v1/TaskInventory` | [docs](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/TaskInventory/put_v1_TaskInventory) |
| [Search Assets](actions/search-assets.md) | `GET /settings/api/v1/Assets/SearchHints` | [docs](https://apigw.intradesk.ru/settings_docs/swagger/index.html#/Assets/get_api_v1_Assets_SearchHints) |
| [Search Clients](actions/search-clients.md) | `GET /settings/api/v1/clients/Search` | [docs](https://apigw.intradesk.ru/settings_docs/swagger/index.html#/Clients/get_api_v1_clients_Search) |
| [Search Employees](actions/search-employees.md) | `GET /settings/api/v1/Employees/SearchHints` | [docs](https://apigw.intradesk.ru/settings_docs/swagger/index.html#/Employees/get_api_v1_Employees_SearchHints) |
| [Search Knowledge Base Articles](actions/search-knowledge-base-articles.md) | `GET /knowledgebase/api/v1/Hints/search` | [docs](https://apigw.intradesk.ru/knowledgebase_docs/swagger/index.html#/Hints/get_api_v1_Hints_search) |
| [Set Task Active State](actions/set-task-active-state.md) | `POST /changes/v1/Tasks/Activate` | [docs](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Tasks/post_v1_Tasks_Activate) |
| [Update Task](actions/update-task.md) | `PUT /changes/v3/Tasks` | [docs](https://apigw.intradesk.ru/changes_docs/swagger/index.html#/Tasks/put_v3_Tasks) |
