# <img src="https://images.mindcloud.co/apps/icons/locu_1774980415338.png" alt="Locu logo" width="28" height="28"> Locu: Universal API

Locu is a focused work workspace for tasks, notes, meetings, timers, and sessions, with a public REST API for managing that data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/locu/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://locu.app
- **Vendor API docs:** https://locu.app/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/locu/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Session Activity](actions/create-session-activity.md) | POST | Creates a new task activity in a Locu session. |
| [Delete Session Activity](actions/delete-session-activity.md) | DELETE | Deletes an existing session activity from Locu. |
| [List Activities](actions/list-activities.md) | GET | Retrieves a paginated list of session activities from Locu. |
| [List Session Activities](actions/list-session-activities.md) | GET | Retrieves activities for a specific session from Locu. |
| [Update Session Activity](actions/update-session-activity.md) | PUT | Updates an existing session activity in Locu. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note in Locu. |
| [Delete Note](actions/delete-note.md) | DELETE | Deletes an existing note from Locu. |
| [Get Note](actions/get-note.md) | GET | Retrieves a single note by ID from Locu. |
| [List Notes](actions/list-notes.md) | GET | Retrieves a paginated list of notes from Locu. |
| [Update Note](actions/update-note.md) | PUT | Updates an existing note in Locu. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Timer](actions/cancel-timer.md) | DELETE | Deletes the current timer from Locu. |
| [Continue Timer](actions/continue-timer.md) | PUT | Updates the Locu timer by resuming it. |
| [Get Timer State](actions/get-timer-state.md) | GET | Retrieves the current timer state from Locu. |
| [Pause Timer](actions/pause-timer.md) | PUT | Updates the Locu timer by pausing it. |
| [Start Timer](actions/start-timer.md) | POST | Starts a new session timer in Locu. |
| [Stop Timer](actions/stop-timer.md) | PUT | Updates the Locu timer by stopping it. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Locu. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Locu. |
| [Get Project](actions/get-project.md) | GET | Retrieves a single project by ID from Locu. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a paginated list of projects from Locu. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Locu. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST | Creates a new work session in Locu. |
| [Delete Session](actions/delete-session.md) | DELETE | Deletes an existing session from Locu. |
| [Get Session](actions/get-session.md) | GET | Retrieves a single session by ID from Locu. |
| [List Sessions](actions/list-sessions.md) | GET | Retrieves a paginated list of sessions from Locu. |
| [Update Session](actions/update-session.md) | PUT | Updates an existing session in Locu. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Locu. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Locu. |
| [Get Task](actions/get-task.md) | GET | Retrieves a single task by ID from Locu. |
| [List Subtasks](actions/list-subtasks.md) | GET | Retrieves subtasks for a task from Locu. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a paginated list of tasks from Locu. |
| [List Tasks By Section](actions/list-tasks-by-section.md) | GET | Retrieves tasks organized by section from Locu. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Locu. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the authenticated user and workspace from Locu. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Locu. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a single webhook by ID from Locu. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a paginated list of webhooks from Locu. |
| [Rotate Webhook Secret](actions/rotate-webhook-secret.md) | PUT | Updates a webhook by rotating its secret in Locu. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Locu. |

### Webhook Delivery

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Deliveries](actions/list-webhook-deliveries.md) | GET | Retrieves recent webhook deliveries from Locu. |

