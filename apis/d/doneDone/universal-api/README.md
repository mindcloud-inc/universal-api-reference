# <img src="https://images.mindcloud.co/apps/icons/dd-logo-512x512-1-150x150_1774893040098.png" alt="DoneDone logo" width="28" height="28"> DoneDone: Universal API

Task management and shared inbox platform for teams to track work, manage projects, and collaborate on customer conversations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/doneDone/latest
- **Category:** Productivity / Project Management
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.donedone.com
- **Vendor API docs:** https://donedone.com/help-docs/public-api-webhooks/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from DoneDone. |

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Task History](actions/get-task-history.md) | GET | Retrieves task history from DoneDone. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Add Task Comment](actions/add-task-comment.md) | POST | Creates a new task comment in DoneDone. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [List Project Priorities](actions/list-project-priorities.md) | GET | Retrieves project priorities from DoneDone. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves project details from DoneDone. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from DoneDone. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Project Statuses](actions/list-project-statuses.md) | GET | Retrieves project statuses from DoneDone. |
| [List Workflow Statuses](actions/list-workflow-statuses.md) | GET | Retrieves workflow statuses from DoneDone. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Project Tags](actions/list-project-tags.md) | GET | Retrieves project tags from DoneDone. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in DoneDone. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from DoneDone. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from DoneDone. |
| [Update Task Priority](actions/update-task-priority.md) | PUT | Updates an existing task priority in DoneDone. |
| [Update Task Status](actions/update-task-status.md) | PUT | Updates an existing task status in DoneDone. |
| [Update Task Title](actions/update-task-title.md) | PUT | Updates an existing task title in DoneDone. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET | Retrieves your DoneDone profile. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves workflow details from DoneDone. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from DoneDone. |

