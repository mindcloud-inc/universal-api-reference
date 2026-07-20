# <img src="https://images.mindcloud.co/apps/icons/nozbe-teams-symbol-only-square_1775741003469.png" alt="Nozbe Teams logo" width="28" height="28"> Nozbe Teams: Universal API

Manage Nozbe Teams teams, projects, tasks, comments, reminders, tags, and related collaboration resources through the official Nozbe API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nozbeTeams/latest
- **Category:** Support / Ticketing
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nozbe.com/teams/
- **Vendor API docs:** https://api4.nozbe.com/v1/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Event](actions/get-task-event.md) | GET | Retrieves a task event from Nozbe Teams. |
| [List Task Events](actions/list-task-events.md) | GET | Retrieves accessible task events from Nozbe Teams. |

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Create Reminder](actions/create-reminder.md) | POST | Creates a new reminder in Nozbe Teams. |
| [Delete Reminder](actions/delete-reminder.md) | DELETE | Deletes an existing reminder from Nozbe Teams. |
| [Get Reminder](actions/get-reminder.md) | GET | Retrieves a reminder from Nozbe Teams. |
| [List Reminders](actions/list-reminders.md) | GET | Retrieves accessible reminders from Nozbe Teams. |

### Columns

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Section](actions/create-project-section.md) | POST | Creates a new project section in Nozbe Teams. |
| [Delete Project Section](actions/delete-project-section.md) | DELETE | Deletes an existing project section from Nozbe Teams. |
| [Get Project Section](actions/get-project-section.md) | GET | Retrieves a project section from Nozbe Teams. |
| [List Project Sections](actions/list-project-sections.md) | GET | Retrieves accessible project sections from Nozbe Teams. |
| [Update Project Section](actions/update-project-section.md) | PUT | Updates an existing project section in Nozbe Teams. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Nozbe Teams. |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes an existing comment from Nozbe Teams. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from Nozbe Teams. |
| [List Comments](actions/list-comments.md) | GET | Retrieves accessible comments from Nozbe Teams. |
| [Update Comment](actions/update-comment.md) | PUT | Updates an existing comment in Nozbe Teams. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Nozbe Teams. |
| [Create Project From Template](actions/create-project-from-template.md) | POST | Creates a new project from a template in Nozbe Teams. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Nozbe Teams. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Nozbe Teams. |
| [List Projects](actions/list-projects.md) | GET | Retrieves accessible projects from Nozbe Teams. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Nozbe Teams. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Nozbe Teams. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Nozbe Teams. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Nozbe Teams. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves accessible tasks from Nozbe Teams. |
| [Poll New Tasks](actions/poll-new-tasks.md) | GET | Retrieves new tasks since the last call in Nozbe Teams. |
| [Poll Updated Tasks](actions/poll-updated-tasks.md) | GET | Retrieves updated tasks since the last call in Nozbe Teams. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Nozbe Teams. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from Nozbe Teams. |
| [List Teams](actions/list-teams.md) | GET | Retrieves accessible teams from Nozbe Teams. |

