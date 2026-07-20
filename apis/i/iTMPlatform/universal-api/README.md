# <img src="https://images.mindcloud.co/apps/icons/i-tmplatform_1775153284377.png" alt="ITM Platform logo" width="28" height="28"> ITM Platform: Universal API

Project, program, and portfolio management software for planning, delivery, resources, risks, financials, and reporting in ITM Platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iTMPlatform/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.itmplatform.com
- **Vendor API docs:** https://developers.itmplatform.com/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authentication](actions/get-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/get-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [List Clients](actions/list-clients.md) | GET |  |

### Issues

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Issue](actions/get-project-issue.md) | GET |  |
| [List Project Issues](actions/list-project-issues.md) | GET |  |
| [List Risk Associated Issue List](actions/list-risk-associated-issue-list.md) | GET |  |
| [List Risk Associated Issues](actions/list-risk-associated-issues.md) | GET |  |
| [Search Issues](actions/search-issues.md) | GET |  |
| [Search Project Issues](actions/search-project-issues.md) | GET |  |

### Programs

| Action | Method | Description |
| --- | --- | --- |
| [List Programs](actions/list-programs.md) | GET |  |
| [Search Programs](actions/search-programs.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |
| [Get Project Budget](actions/get-project-budget.md) | GET |  |
| [List Project Change History](actions/list-project-change-history.md) | GET |  |
| [List Project Progress Reports](actions/list-project-progress-reports.md) | GET |  |
| [List Project Swimlanes](actions/list-project-swimlanes.md) | GET |  |
| [List Project Team](actions/list-project-team.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Search Projects](actions/search-projects.md) | GET |  |

### Risk

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Risk](actions/get-project-risk.md) | GET |  |
| [List Issue Risks](actions/list-issue-risks.md) | GET |  |
| [List Project Risks](actions/list-project-risks.md) | GET |  |
| [Search Project Risks](actions/search-project-risks.md) | GET |  |
| [Search Risks](actions/search-risks.md) | GET |  |

### Risk Manager

| Action | Method | Description |
| --- | --- | --- |
| [List Project Risk Managers](actions/list-project-risk-managers.md) | GET |  |

### Risk Occurrence Management

| Action | Method | Description |
| --- | --- | --- |
| [Get Risk Occurrence Management](actions/get-risk-occurrence-management.md) | GET |  |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Get Authentication](actions/get-authentication.md) | GET |  |

### Sprints

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Sprint](actions/get-project-sprint.md) | GET |  |
| [List Allocated Tasks For Sprint](actions/list-allocated-tasks-for-sprint.md) | GET |  |
| [Search Project Sprints](actions/search-project-sprints.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Gantt](actions/get-project-gantt.md) | GET |  |
| [Get Task](actions/get-task.md) | GET |  |
| [Get Task Effort by Professional Category](actions/get-task-effort-by-professional-category.md) | GET |  |
| [Get Task Effort by Team Member](actions/get-task-effort-by-team-member.md) | GET |  |
| [Get Task Progress Report](actions/get-task-progress-report.md) | GET |  |
| [List Agile Task Statuses](actions/list-agile-task-statuses.md) | GET |  |
| [List Task Dependencies](actions/list-task-dependencies.md) | GET |  |
| [List Task Progress Reports](actions/list-task-progress-reports.md) | GET |  |
| [List Task Team](actions/list-task-team.md) | GET |  |
| [Search Project Tasks](actions/search-project-tasks.md) | GET |  |
| [Search Tasks](actions/search-tasks.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET |  |

