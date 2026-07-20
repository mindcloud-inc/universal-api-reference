# <img src="https://images.mindcloud.co/apps/icons/microsoft-planner-2024present_1776197312994.png" alt="Microsoft 365 Planner logo" width="28" height="28"> Microsoft 365 Planner: Universal API

Access Microsoft 365 Planner data through Microsoft Graph, including plans, buckets, tasks, and task details for work or school accounts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoft365Planner/latest
- **Category:** Productivity / Project Management
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://planner.cloud.microsoft
- **Vendor API docs:** https://learn.microsoft.com/en-us/graph/api/resources/planner-overview?view=graph-rest-1.0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Microsoft 365 Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET |  |

### Microsoft 365 Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET |  |

### Planner Bucket

| Action | Method | Description |
| --- | --- | --- |
| [Create Bucket](actions/create-bucket.md) | POST |  |
| [Get Bucket](actions/get-bucket.md) | GET |  |

### Planner Buckets

| Action | Method | Description |
| --- | --- | --- |
| [List Plan Buckets](actions/list-plan-buckets.md) | GET |  |

### Planner Plan

| Action | Method | Description |
| --- | --- | --- |
| [Create Plan](actions/create-plan.md) | POST |  |
| [Get Plan](actions/get-plan.md) | GET |  |

### Planner Plan Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan Details](actions/get-plan-details.md) | GET |  |

### Planner Plans

| Action | Method | Description |
| --- | --- | --- |
| [List Group Plans](actions/list-group-plans.md) | GET |  |
| [List My Plans](actions/list-my-plans.md) | GET |  |

### Planner Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Get Task](actions/get-task.md) | GET |  |

### Planner Task Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Details](actions/get-task-details.md) | GET |  |

### Planner Tasks

| Action | Method | Description |
| --- | --- | --- |
| [List Plan Tasks](actions/list-plan-tasks.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET |  |

