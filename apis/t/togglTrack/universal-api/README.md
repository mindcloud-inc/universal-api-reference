# <img src="https://images.mindcloud.co/apps/icons/toggle_1773176573624.png" alt="Toggl Track logo" width="28" height="28"> Toggl Track: Universal API

Track time entries, projects, tasks, clients, tags, workspace data, and reports in Toggl Track.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/togglTrack/latest
- **Category:** Productivity / Project Management
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://toggl.com/track/
- **Vendor API docs:** https://engineering.toggl.com/docs/track/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Archive Client](actions/archive-client.md) | PUT | Archives an existing client in Toggl Track. |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Toggl Track. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Toggl Track. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from a Toggl Track workspace. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Toggl Track. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Toggl Track. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Toggl Track. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Toggl Track. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from a Toggl Track workspace. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Toggl Track. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Search Detailed Report](actions/search-detailed-report.md) | GET | Finds detailed report time entries in Toggl Track. |
| [Search Summary Report](actions/search-summary-report.md) | GET | Finds summary report time entries in Toggl Track. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Toggl Track. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Toggl Track. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from a Toggl Track workspace. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Toggl Track. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Toggl Track. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Toggl Track. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Toggl Track. |
| [List Project Tasks](actions/list-project-tasks.md) | GET | Retrieves tasks for a Toggl Track project. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Toggl Track. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in Toggl Track. |
| [Delete Time Entry](actions/delete-time-entry.md) | DELETE | Deletes an existing time entry from Toggl Track. |
| [Get Current Time Entry](actions/get-current-time-entry.md) | GET | Retrieves the current time entry from Toggl Track. |
| [Get Time Entry By ID](actions/get-time-entry-by-id.md) | GET | Retrieves a time entry by ID from Toggl Track. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from Toggl Track. |
| [Stop Time Entry](actions/stop-time-entry.md) | PUT | Stops an existing time entry in Toggl Track. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in Toggl Track. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Toggl Track. |
| [Get Workspace Users](actions/get-workspace-users.md) | GET | Retrieves workspace users from Toggl Track. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from Toggl Track. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Toggl Track. |

