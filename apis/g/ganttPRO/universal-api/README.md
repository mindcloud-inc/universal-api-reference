# <img src="https://images.mindcloud.co/apps/icons/gantt-pro_1778086719797.png" alt="GanttPRO logo" width="28" height="28"> GanttPRO: Universal API

Connect GanttPRO to read and manage projects, tasks, resources, comments, attachments, links, roles, and time logs through the official GanttPRO REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ganttPRO/latest
- **Category:** Support / Ticketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ganttpro.com/
- **Vendor API docs:** https://developer.ganttpro.com/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Attachment](actions/delete-attachment.md) | DELETE | Deletes an existing attachment from GanttPRO. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Comment](actions/create-task-comment.md) | POST | Creates a new comment on a GanttPRO task. |
| [Delete Task Comment](actions/delete-task-comment.md) | DELETE | Deletes an existing task comment from GanttPRO. |
| [List Project Comments](actions/list-project-comments.md) | GET | Retrieves comments for a specific GanttPRO project. |
| [List Task Comments](actions/list-task-comments.md) | GET | Retrieves comments for a specific GanttPRO task. |
| [Update Task Comment](actions/update-task-comment.md) | PUT | Updates an existing task comment in GanttPRO. |

### Custom Day

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Custom Day](actions/create-project-custom-day.md) | POST | Creates a custom day in a GanttPRO project calendar. |
| [Delete Project Custom Day](actions/delete-project-custom-day.md) | DELETE | Deletes a custom day from a GanttPRO project calendar. |
| [Update Project Custom Day](actions/update-project-custom-day.md) | PUT | Updates a custom day in a GanttPRO project calendar. |

### Notification Setting

| Action | Method | Description |
| --- | --- | --- |
| [Update User Notification Settings](actions/update-user-notification-settings.md) | PUT | Updates notification settings for a GanttPRO user. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from your GanttPRO account. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from your GanttPRO account. |

### Project Calendar

| Action | Method | Description |
| --- | --- | --- |
| [List Project Calendars](actions/list-project-calendars.md) | GET | Retrieves project calendars from your GanttPRO account. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [List Resources](actions/list-resources.md) | GET | Retrieves resources from your GanttPRO account. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in GanttPRO. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from GanttPRO. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from your GanttPRO account. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from a specific GanttPRO project. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in GanttPRO. |

### Task Field

| Action | Method | Description |
| --- | --- | --- |
| [List Project Task Fields](actions/list-project-task-fields.md) | GET | Retrieves task fields for a specific GanttPRO project. |

### Task Resource Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Assign Resource To Task](actions/assign-resource-to-task.md) | POST | Assigns resources to an existing GanttPRO task. |
| [Remove Resource From Task](actions/remove-resource-from-task.md) | DELETE | Removes resources from an existing GanttPRO task. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Team](actions/get-current-team.md) | GET | Retrieves the current team from GanttPRO. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from your GanttPRO account. |

