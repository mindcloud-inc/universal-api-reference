# <img src="https://images.mindcloud.co/apps/icons/5ac2f2b3-e035-4b88-98d5-724c8e04b21f_1773852684242.png" alt="ActiveCollab logo" width="28" height="28"> ActiveCollab: Universal API

Manage ActiveCollab projects, tasks, discussions, and time records

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/activeCollab/latest
- **Category:** Productivity / Project Management
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://activecollab.com
- **Vendor API docs:** https://developers.activecollab.com/api-documentation/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeCollab/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from your ActiveCollab workspace. |
| [List Companies](actions/list-companies.md) | GET | Retrieves all companies from your ActiveCollab workspace. |

### Discussion

| Action | Method | Description |
| --- | --- | --- |
| [List Discussions](actions/list-discussions.md) | GET | Retrieves discussions for a project in ActiveCollab. |

### Job Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Job Type](actions/get-default-job-type.md) | GET | Retrieves the default job type from ActiveCollab. |
| [List Job Types](actions/list-job-types.md) | GET | Retrieves job types from your ActiveCollab workspace. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [List Labels](actions/list-labels.md) | GET | Retrieves predefined labels from your ActiveCollab workspace. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes for a project in ActiveCollab. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in ActiveCollab. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from ActiveCollab. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from your ActiveCollab workspace. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all projects from your ActiveCollab workspace. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in ActiveCollab. |

### Project Label

| Action | Method | Description |
| --- | --- | --- |
| [List Project Labels](actions/list-project-labels.md) | GET | Retrieves project labels from your ActiveCollab workspace. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks for a project in ActiveCollab. |

### Task List

| Action | Method | Description |
| --- | --- | --- |
| [List Task Lists](actions/list-task-lists.md) | GET | Retrieves task lists for a project in ActiveCollab. |

### Time Record

| Action | Method | Description |
| --- | --- | --- |
| [List Project Time Records](actions/list-project-time-records.md) | GET | Retrieves time records for a project in ActiveCollab. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from your ActiveCollab workspace. |
| [List Users](actions/list-users.md) | GET | Retrieves all users from your ActiveCollab workspace. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace Info](actions/get-workspace-info.md) | GET | Retrieves application details from your ActiveCollab workspace. |

