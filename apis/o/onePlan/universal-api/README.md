# <img src="https://images.mindcloud.co/apps/icons/images-30_1776984049677.png" alt="OnePlan logo" width="28" height="28"> OnePlan: Universal API

OnePlan is a strategic portfolio and work management platform for plans, resources, tasks, status reports, costs, integrations, and portfolio execution data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/onePlan/latest
- **Category:** Productivity / Project Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://oneplan.ai/
- **Vendor API docs:** https://my.oneplan.ai/ApiHelp

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Security Groups](actions/get-security-groups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-security-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Child Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get Child Plans](actions/get-child-plans.md) | GET | Retrieves child plans from OnePlan. |

### Cost Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Cost Categories Tree](actions/get-cost-categories-tree.md) | GET | Retrieves the cost categories tree from OnePlan. |

### Enterprise Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Enterprise Team](actions/get-enterprise-team.md) | GET | Retrieves an enterprise team from OnePlan. |
| [List Enterprise Teams](actions/list-enterprise-teams.md) | GET | Retrieves enterprise teams from OnePlan. |
| [List My Enterprise Teams](actions/list-my-enterprise-teams.md) | GET | Retrieves your enterprise teams from OnePlan. |

### Enterprise Team Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Enterprise Team Members](actions/get-enterprise-team-members.md) | GET | Retrieves enterprise team members from OnePlan. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves events from OnePlan. |

### Event Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Logs](actions/get-event-logs.md) | GET | Retrieves event logs from OnePlan. |

### My Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get My Activities](actions/get-my-activities.md) | GET | Retrieves your activities from OnePlan. |

### My Work Status Field

| Action | Method | Description |
| --- | --- | --- |
| [Get My Work Status Fields](actions/get-my-work-status-fields.md) | GET | Retrieves My Work status fields from OnePlan. |

### My Work Task

| Action | Method | Description |
| --- | --- | --- |
| [Get My Work Tasks](actions/get-my-work-tasks.md) | GET | Retrieves My Work tasks from OnePlan. |

### My Work Update

| Action | Method | Description |
| --- | --- | --- |
| [Get My Work Update](actions/get-my-work-update.md) | GET | Retrieves a My Work update from OnePlan. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get All Plans](actions/get-all-plans.md) | GET | Retrieves plans from OnePlan. |

### Plan Level Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan Level Fields](actions/get-plan-level-fields.md) | GET | Retrieves plan-level fields from OnePlan. |

### Plan Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Tasks For Plan](actions/get-tasks-for-plan.md) | GET | Retrieves tasks for a plan from OnePlan. |

### Plan Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team List For Plan](actions/get-team-list-for-plan.md) | GET | Retrieves shared teams for a plan from OnePlan. |

### Plan User

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan User List](actions/get-plan-user-list.md) | GET | Retrieves plan users from OnePlan. |

### Process History

| Action | Method | Description |
| --- | --- | --- |
| [Get Process History](actions/get-process-history.md) | GET | Retrieves process history from OnePlan. |

### Security Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Security Groups](actions/get-security-groups.md) | GET | Retrieves security groups from OnePlan. |

### Status Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Report For Plan](actions/get-latest-report-for-plan.md) | GET | Retrieves the latest report for a plan from OnePlan. |
| [Get My Status Reports](actions/get-my-status-reports.md) | GET | Retrieves your status reports from OnePlan. |

### Status Report Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Get Status Report PDF](actions/get-status-report-pdf.md) | GET | Retrieves a status report PDF from OnePlan. |

### Status Report Ppt

| Action | Method | Description |
| --- | --- | --- |
| [Get Status Report PPT](actions/get-status-report-ppt.md) | GET | Retrieves a status report PowerPoint from OnePlan. |

### Status Report Word

| Action | Method | Description |
| --- | --- | --- |
| [Get Status Report Word](actions/get-status-report-word.md) | GET | Retrieves a status report Word document from OnePlan. |

### Submitted Status Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Submitted Reports For Approval](actions/get-submitted-reports-for-approval.md) | GET | Retrieves submitted reports for approval from OnePlan. |

### Work Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Work Types For Plan](actions/get-work-types-for-plan.md) | GET | Retrieves work types for a plan from OnePlan. |

### Workplan

| Action | Method | Description |
| --- | --- | --- |
| [Get Workplan By ID](actions/get-workplan-by-id.md) | GET | Retrieves a workplan from OnePlan. |

### Workplan Fragment

| Action | Method | Description |
| --- | --- | --- |
| [List Workplan Fragments](actions/list-workplan-fragments.md) | GET | Retrieves workplan fragments from OnePlan. |

### Workplan User Level

| Action | Method | Description |
| --- | --- | --- |
| [Get Workplan User Levels](actions/get-workplan-user-levels.md) | GET | Retrieves workplan user levels from OnePlan. |

### Workplan Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Workplan Versions](actions/get-workplan-versions.md) | GET | Retrieves workplan versions from OnePlan. |

