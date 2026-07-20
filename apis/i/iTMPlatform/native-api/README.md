# ITM Platform: Native API Reference

A consolidated summary of ITM Platform's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.itmplatform.com/documentation/
- **OpenAPI specification:** https://developers.itmplatform.com/documentation/openapi.json
- **API base URL:** `https://api.itmplatform.com/{company}`

## Authentication

### API Key

Connect with your ITM Platform company URL and API key.

### Credentials

- **API Key:** `apiKey` · required
- **Company URL:** `company` · required · Your ITM Platform account URL segment used in API paths, for example mycompany.

Send these headers with each API request:

```http
Token: <apiKey>
```

[Official authentication documentation](https://helpcenter.itmplatform.com/integrations/API/)

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 1–500). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the request body. Supported operators: `bt`, `eq`, `gt`, `gte`, `in`, `lt`, `lte`, `ne`, `nin`, `regex`.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortOrder`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Authentication](actions/get-authentication.md) | `GET /login/{APIKey}` | [docs](https://developers.itmplatform.com/documentation/#/operations/getAuthentication) |
| [Get Project](actions/get-project.md) | `GET /v2/projects/{ProjectId}` | [docs](https://developers.itmplatform.com/documentation/#/operations/getAProjectV2) |
| [Get Project Budget](actions/get-project-budget.md) | `GET /project/{ProjectId}/budget` | [docs](https://developers.itmplatform.com/documentation/#/operations/getAProjectBudget) |
| [Get Project Gantt](actions/get-project-gantt.md) | `GET /Projects/{ProjectId}/Tasks/Gantt` | [docs](https://developers.itmplatform.com/documentation/#/operations/getGantt) |
| [Get Project Issue](actions/get-project-issue.md) | `GET /v2/Projects/{ProjectId}/Issues/{IssueId}` | [docs](https://developers.itmplatform.com/documentation/#/operations/getAProjectIssueV2) |
| [Get Project Risk](actions/get-project-risk.md) | `GET /v2/Projects/{ProjectId}/Risks/{RiskId}` | [docs](https://developers.itmplatform.com/documentation/#/operations/getAProjectRiskV2) |
| [Get Project Sprint](actions/get-project-sprint.md) | `GET /v2/Projects/{ProjectId}/Sprints/{SprintId}` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProjectSprint) |
| [Get Risk Occurrence Management](actions/get-risk-occurrence-management.md) | `GET /project/{ProjectId}/Issue/{IssueId}/riskoccurencemanagement` | [docs](https://developers.itmplatform.com/documentation/#/operations/getRiskOccurrenceManagement) |
| [Get Task](actions/get-task.md) | `GET /Projects/{ProjectId}/Tasks/{TaskId}` | [docs](https://developers.itmplatform.com/documentation/#/operations/getATask) |
| [Get Task Effort by Professional Category](actions/get-task-effort-by-professional-category.md) | `GET /project/{ProjectId}/task/{TaskId}/effortbyprofessionalcategory` | [docs](https://developers.itmplatform.com/documentation/#/operations/getTaskEffortByProfessionalCategory) |
| [Get Task Effort by Team Member](actions/get-task-effort-by-team-member.md) | `GET /project/{ProjectId}/task/{TaskId}/effortbyteammember` | [docs](https://developers.itmplatform.com/documentation/#/operations/getTaskEffortWorkByTeamMember) |
| [Get Task Progress Report](actions/get-task-progress-report.md) | `GET /project/{ProjectId}/task/{TaskId}/progress/{TaskProgressId}` | [docs](https://developers.itmplatform.com/documentation/#/operations/getATaskProgressReport) |
| [List Agile Task Statuses](actions/list-agile-task-statuses.md) | `GET /v2/Projects/{ProjectId}/GetKanbanTaskStatus` | [docs](https://developers.itmplatform.com/documentation/#/operations/getAgileTaskStatusesV2) |
| [List Allocated Tasks For Sprint](actions/list-allocated-tasks-for-sprint.md) | `GET /v2/Projects/{ProjectId}/AllocatedTasks/{SprintId}` | [docs](https://developers.itmplatform.com/documentation/#/operations/getAllocatedTasksForSprint) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://developers.itmplatform.com/documentation/#/operations/getClients) |
| [List Issue Risks](actions/list-issue-risks.md) | `GET /v2/Projects/{ProjectId}/Issues/{IssueId}/Risks` | [docs](https://developers.itmplatform.com/documentation/#/operations/getAssociatedProjectRiskV2) |
| [List Programs](actions/list-programs.md) | `GET /v2/programs` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProgramsV2) |
| [List Project Change History](actions/list-project-change-history.md) | `GET /Projects/{ProjectId}/changeHistory` | [docs](https://developers.itmplatform.com/documentation/#/operations/changeHistory) |
| [List Project Issues](actions/list-project-issues.md) | `GET /v2/Projects/{ProjectId}/Issues` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProjectIssuesV2) |
| [List Project Progress Reports](actions/list-project-progress-reports.md) | `GET /project/{ProjectId}/progress/` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProjectProgressReport) |
| [List Project Risk Managers](actions/list-project-risk-managers.md) | `GET /project/{ProjectId}/riskmanagers` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProjectRiskManagers) |
| [List Project Risks](actions/list-project-risks.md) | `GET /v2/Projects/{ProjectId}/Risks` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProjectRisksV2) |
| [List Project Swimlanes](actions/list-project-swimlanes.md) | `GET /project/{ProjectId}/swimlanes` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProjectSwimlanes) |
| [List Project Team](actions/list-project-team.md) | `GET /project/{ProjectId}/team` | [docs](https://developers.itmplatform.com/documentation/#/operations/getAProjectTeam) |
| [List Projects](actions/list-projects.md) | `GET /v2/projects` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProjectsV2) |
| [List Risk Associated Issue List](actions/list-risk-associated-issue-list.md) | `GET /project/{ProjectId}/Risk/{RiskId}/AssociatedIssueList` | [docs](https://developers.itmplatform.com/documentation/#/operations/getAssociatedProjectIssueList) |
| [List Risk Associated Issues](actions/list-risk-associated-issues.md) | `GET /project/{ProjectId}/Risk/{RiskId}/AssociatedIssues` | [docs](https://developers.itmplatform.com/documentation/#/operations/getAssociatedIssuesOfRisk) |
| [List Task Dependencies](actions/list-task-dependencies.md) | `GET /project/{ProjectId}/taskdependencies` | [docs](https://developers.itmplatform.com/documentation/#/operations/getTaskDependencies) |
| [List Task Progress Reports](actions/list-task-progress-reports.md) | `GET /project/{ProjectId}/task/{TaskId}/progress/` | [docs](https://developers.itmplatform.com/documentation/#/operations/getTaskProgressReports) |
| [List Task Team](actions/list-task-team.md) | `GET /project/{ProjectId}/task/{TaskId}/team//` | [docs](https://developers.itmplatform.com/documentation/#/operations/getATaskTeam) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.itmplatform.com/documentation/#/operations/getUsers) |
| [Search Issues](actions/search-issues.md) | `GET /v2/issues/search` | [docs](https://developers.itmplatform.com/documentation/#/operations/getIssuesV2) |
| [Search Programs](actions/search-programs.md) | `POST /v2/programs/search` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProgramV2) |
| [Search Project Issues](actions/search-project-issues.md) | `GET /v2/Projects/{ProjectId}/Issues/Search` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProjectIssuesSearchV2) |
| [Search Project Risks](actions/search-project-risks.md) | `GET /v2/Projects/{ProjectId}/Risks/Search` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProjectRisksSearchV2) |
| [Search Project Sprints](actions/search-project-sprints.md) | `POST /v2/Projects/{ProjectId}/Sprints/Search` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProjectSprintSearch) |
| [Search Project Tasks](actions/search-project-tasks.md) | `POST /Projects/{ProjectId}/Tasks/Search` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProjectTasksSearch) |
| [Search Projects](actions/search-projects.md) | `POST /v2/projects/search` | [docs](https://developers.itmplatform.com/documentation/#/operations/getProjectsV2_1) |
| [Search Risks](actions/search-risks.md) | `GET /v2/risks/search` | [docs](https://developers.itmplatform.com/documentation/#/operations/getRisksV2) |
| [Search Tasks](actions/search-tasks.md) | `POST /v2/tasks/search` | [docs](https://developers.itmplatform.com/documentation/#/operations/getTasksV2) |
