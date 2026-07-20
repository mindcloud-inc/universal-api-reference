# <img src="https://images.mindcloud.co/apps/icons/good-daywork_1774536631129.png" alt="GoodDay.work logo" width="28" height="28"> GoodDay.work: Universal API

Manage projects, tasks, events, CRM, and team collaboration

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/goodDaywork/latest
- **Category:** Productivity / Project Management
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.goodday.work
- **Vendor API docs:** https://www.goodday.work/developers/api-v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Finds custom fields in the GoodDay.work workspace. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves a single document from GoodDay.work. |
| [List Project Documents](actions/list-project-documents.md) | GET | Finds documents in a GoodDay.work project. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in GoodDay.work. |
| [Delete Event](actions/delete-event.md) | DELETE | Deletes an existing event from GoodDay.work. |
| [Get Event](actions/get-event.md) | GET | Retrieves a single event from GoodDay.work. |
| [List Events](actions/list-events.md) | GET | Finds events in the GoodDay.work workspace. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in GoodDay.work. |

### Office

| Action | Method | Description |
| --- | --- | --- |
| [List Offices](actions/list-offices.md) | GET | Finds offices in the GoodDay.work workspace. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in GoodDay.work. |
| [Get Project](actions/get-project.md) | GET | Retrieves a single project from GoodDay.work. |
| [List Projects](actions/list-projects.md) | GET | Finds projects in the GoodDay.work workspace. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in GoodDay.work. |

### Project History

| Action | Method | Description |
| --- | --- | --- |
| [List Project History](actions/list-project-history.md) | GET | Finds history entries for a GoodDay.work project. |

### Skill

| Action | Method | Description |
| --- | --- | --- |
| [List Skills](actions/list-skills.md) | GET | Finds skills in the GoodDay.work workspace. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [List Statuses](actions/list-statuses.md) | GET | Finds statuses in the GoodDay.work workspace. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in GoodDay.work. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from GoodDay.work. |
| [Get Task](actions/get-task.md) | GET | Retrieves a single task from GoodDay.work. |
| [List Project Tasks](actions/list-project-tasks.md) | GET | Finds tasks in a GoodDay.work project. |
| [List Tag Tasks](actions/list-tag-tasks.md) | GET | Finds tasks with a specific GoodDay.work tag. |
| [List User Action Required Tasks](actions/list-user-action-required-tasks.md) | GET | Finds tasks requiring action from a GoodDay.work user. |
| [List User Assigned Tasks](actions/list-user-assigned-tasks.md) | GET | Finds tasks assigned to a GoodDay.work user. |
| [Update Task Status](actions/update-task-status.md) | PUT | Updates the status of a GoodDay.work task. |

### Task Comment

| Action | Method | Description |
| --- | --- | --- |
| [Comment On Task](actions/comment-on-task.md) | POST | Creates a comment on a GoodDay.work task. |

### Task Message

| Action | Method | Description |
| --- | --- | --- |
| [List Task Messages](actions/list-task-messages.md) | GET | Finds messages on a GoodDay.work task. |

### Task Type

| Action | Method | Description |
| --- | --- | --- |
| [List Task Types](actions/list-task-types.md) | GET | Finds task types in the GoodDay.work workspace. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a single user from GoodDay.work. |
| [List Project Users](actions/list-project-users.md) | GET | Finds users in a GoodDay.work project. |
| [List Users](actions/list-users.md) | GET | Finds users in the GoodDay.work workspace. |

### User Hourly Rate History

| Action | Method | Description |
| --- | --- | --- |
| [List User Hourly Rate History](actions/list-user-hourly-rate-history.md) | GET | Retrieves hourly rate history from GoodDay.work for a user. |

