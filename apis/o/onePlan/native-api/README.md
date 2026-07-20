# OnePlan: Native API Reference

A consolidated summary of OnePlan's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://my.oneplan.ai/ApiHelp
- **API base URL:** `https://my.oneplan.ai/api`

## Authentication

### OnePlan Authentication Key

Authenticate with the OnePlan key name as the username and the generated Authentication Key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://support.oneplan.ai/hc/en-us/articles/10998192052749-OnePlan-Configuration-Integration-Page)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get All Plans](actions/get-all-plans.md) | `GET /workplan` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan_FilterField_FilterValue_ShowArchived_ShowTemplates_BuiltInField_EditOnly) |
| [Get Child Plans](actions/get-child-plans.md) | `GET /workplan/{PlanId}/subplans` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan-PlanId-subplans) |
| [Get Cost Categories Tree](actions/get-cost-categories-tree.md) | `GET /cost/tree` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-cost-tree) |
| [Get Enterprise Team](actions/get-enterprise-team.md) | `GET /enterpriseteams/{id}` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-enterpriseteams-id) |
| [Get Enterprise Team Members](actions/get-enterprise-team-members.md) | `GET /enterpriseteams/{id}/members` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-enterpriseteams-id-members) |
| [Get Event Logs](actions/get-event-logs.md) | `GET /events/{Id}/log` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-events-Id-log) |
| [Get Latest Report For Plan](actions/get-latest-report-for-plan.md) | `GET /statusreports/{PlanId}` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-statusreports-PlanId_ReportId) |
| [Get My Activities](actions/get-my-activities.md) | `GET /mywork/activities` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-mywork-activities) |
| [Get My Status Reports](actions/get-my-status-reports.md) | `GET /statusreports/my` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-statusreports-my_States%5B0%5D_States%5B1%5D) |
| [Get My Work Status Fields](actions/get-my-work-status-fields.md) | `GET /mywork/statusfields` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-mywork-statusfields) |
| [Get My Work Tasks](actions/get-my-work-tasks.md) | `GET /mywork/tasks` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-mywork-tasks_PeriodStart_PeriodEnd_ShowComplete_UserId) |
| [Get My Work Update](actions/get-my-work-update.md) | `GET /mywork/getupdate/{id}` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-mywork-getupdate-id) |
| [Get Plan Level Fields](actions/get-plan-level-fields.md) | `GET /workplan/fields` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan-fields_HideSystem) |
| [Get Plan User List](actions/get-plan-user-list.md) | `GET /workplan/{PlanId}/user` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan-PlanId-user) |
| [Get Process History](actions/get-process-history.md) | `GET /workplan/{PlanId}/processhistory` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan-PlanId-processhistory) |
| [Get Security Groups](actions/get-security-groups.md) | `GET /securitygroups` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-securitygroups) |
| [Get Status Report PDF](actions/get-status-report-pdf.md) | `GET /statusreports/{id}/pdf` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-statusreports-id-pdf) |
| [Get Status Report PPT](actions/get-status-report-ppt.md) | `GET /statusreports/{id}/ppt` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-statusreports-id-ppt) |
| [Get Status Report Word](actions/get-status-report-word.md) | `GET /statusreports/{id}/doc` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-statusreports-id-doc) |
| [Get Submitted Reports For Approval](actions/get-submitted-reports-for-approval.md) | `GET /statusreports/mysubmit` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-statusreports-mysubmit) |
| [Get Tasks For Plan](actions/get-tasks-for-plan.md) | `GET /workplan/{id}/tasks` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan-id-tasks_HasUpdates_FilterField_FilterValue_BuiltInField) |
| [Get Team List For Plan](actions/get-team-list-for-plan.md) | `GET /workplan/{PlanId}/sharedwithteam` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan-PlanId-sharedwithteam) |
| [Get Work Types For Plan](actions/get-work-types-for-plan.md) | `GET /workplan/{PlanId}/worktypes` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan-PlanId-worktypes) |
| [Get Workplan By ID](actions/get-workplan-by-id.md) | `GET /workplan/{PlanId}` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan-PlanId) |
| [Get Workplan User Levels](actions/get-workplan-user-levels.md) | `GET /workplan/user/levels` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan-user-levels) |
| [Get Workplan Versions](actions/get-workplan-versions.md) | `GET /workplan/{id}/versions` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan-id-versions) |
| [List Enterprise Teams](actions/list-enterprise-teams.md) | `GET /enterpriseteams` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-enterpriseteams) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-events_List) |
| [List My Enterprise Teams](actions/list-my-enterprise-teams.md) | `GET /enterpriseteams/list/my` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-enterpriseteams-list-my) |
| [List Workplan Fragments](actions/list-workplan-fragments.md) | `GET /workplan/fragments` | [docs](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan-fragments_FragmentCategory) |
