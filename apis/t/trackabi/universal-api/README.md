# <img src="https://images.mindcloud.co/apps/icons/trackabi_1775659962675.png" alt="Trackabi logo" width="28" height="28"> Trackabi: Universal API

Track time, manage projects, and log leave

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trackabi/latest
- **Category:** Human Resources / HRIS
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://trackabi.com
- **Vendor API docs:** https://trackabi.com/help/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Details](actions/get-company-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-company-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Trackabi. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from Trackabi. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Trackabi. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Trackabi. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Trackabi. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Details](actions/get-company-details.md) | GET | Retrieves company details from Trackabi. |

### Leave

| Action | Method | Description |
| --- | --- | --- |
| [List Leaves](actions/list-leaves.md) | GET | Retrieves company leave records from Trackabi. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Members](actions/list-members.md) | GET | Retrieves company members from Trackabi. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Assign Project Members](actions/assign-project-members.md) | PUT | Assigns members to a project in Trackabi. |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Trackabi. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Trackabi. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Trackabi. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Trackabi. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Trackabi. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in a Trackabi project. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Trackabi. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Trackabi. |
| [List Project Tasks](actions/list-project-tasks.md) | GET | Retrieves tasks for a project from Trackabi. |
| [List Task Subtasks](actions/list-task-subtasks.md) | GET | Retrieves subtasks for a task from Trackabi. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Trackabi. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Trackabi. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in Trackabi. |
| [Delete Time Entry](actions/delete-time-entry.md) | DELETE | Deletes an existing time entry from Trackabi. |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from Trackabi. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from Trackabi. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in Trackabi. |

### Time Type

| Action | Method | Description |
| --- | --- | --- |
| [List Time Types](actions/list-time-types.md) | GET | Retrieves time types from Trackabi. |

