# <img src="https://images.mindcloud.co/apps/icons/5ea1b3e904575bd504a5d6c119d5ab0f_1781293442024.png" alt="CheckFlow logo" width="28" height="28"> CheckFlow: Universal API

Create recurring checklists, workflows, and standard operating procedures

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/checkFlow/latest
- **Category:** Productivity / Project Management
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://checkflow.io
- **Vendor API docs:** https://docs.checkflow.io/docs/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Team Members](actions/list-team-members.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-team-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Analytics Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Analytics](actions/get-analytics.md) | GET |  |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Validate API Key](actions/validate-api-key.md) | GET |  |

### Assignee

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members And Groups](actions/list-team-members-and-groups.md) | GET |  |

### Checklist

| Action | Method | Description |
| --- | --- | --- |
| [Create Checklist](actions/create-checklist.md) | POST |  |
| [Create Checklist With Parameters](actions/create-checklist-with-parameters.md) | POST |  |
| [Create Many Checklists](actions/create-many-checklists.md) | POST |  |
| [Delete Checklist](actions/delete-checklist.md) | DELETE |  |
| [Delete Many Checklists](actions/delete-many-checklists.md) | DELETE |  |
| [Find Checklists](actions/find-checklists.md) | GET |  |
| [Get Checklist Details](actions/get-checklist-details.md) | GET |  |
| [Share Checklist](actions/share-checklist.md) | PUT |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [List Team Groups](actions/list-team-groups.md) | GET |  |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET |  |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Assign Tag To Checklist Or Task](actions/assign-tag-to-checklist-or-task.md) | POST |  |
| [Create Tag](actions/create-tag.md) | POST |  |
| [Delete Tag](actions/delete-tag.md) | DELETE |  |
| [List Tags](actions/list-tags.md) | GET |  |
| [Remove Tag Assignment](actions/remove-tag-assignment.md) | DELETE |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Add Task Assignees by Name](actions/add-task-assignees-by-name.md) | PUT |  |
| [Get Task Details](actions/get-task-details.md) | GET |  |
| [List Tasks by Task Key](actions/list-tasks-by-task-key.md) | GET |  |
| [Update Task Status](actions/update-task-status.md) | PUT |  |

### Task Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Task Assignments](actions/delete-task-assignments.md) | DELETE |  |
| [List Task Assignments](actions/list-task-assignments.md) | GET |  |
| [Update Task Assignments](actions/update-task-assignments.md) | PUT |  |

### Task Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Comment](actions/create-task-comment.md) | POST |  |

### Task Content

| Action | Method | Description |
| --- | --- | --- |
| [Update Task Control Value](actions/update-task-control-value.md) | PUT |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET |  |

### Template Task

| Action | Method | Description |
| --- | --- | --- |
| [List Template Tasks](actions/list-template-tasks.md) | GET |  |

### Template Task Content

| Action | Method | Description |
| --- | --- | --- |
| [List Task Controls](actions/list-task-controls.md) | GET |  |

### Uploaded File

| Action | Method | Description |
| --- | --- | --- |
| [Get Uploaded Checklist Files](actions/get-uploaded-checklist-files.md) | GET |  |

### Webhook Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST |  |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET |  |

