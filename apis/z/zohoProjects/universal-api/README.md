# <img src="https://images.mindcloud.co/apps/icons/zoho-projects_1773685111884.png" alt="Zoho Projects logo" width="28" height="28"> Zoho Projects: Universal API

Manage Zoho Projects portals, projects, task lists, tasks, issues, and users through the Zoho Projects V3 API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoProjects/latest
- **Category:** Support / Ticketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/projects/
- **Vendor API docs:** https://projectsapi.zoho.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Portals](actions/list-portals.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-portals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Checklists

| Action | Method | Description |
| --- | --- | --- |
| [Create Task List](actions/create-task-list.md) | POST | Creates a new task list in Zoho Projects. |
| [Delete Task List](actions/delete-task-list.md) | DELETE | Deletes an existing task list from Zoho Projects. |
| [Get Task List Details](actions/get-task-list-details.md) | GET | Retrieves task list details from Zoho Projects. |
| [List Project Task Lists](actions/list-project-task-lists.md) | GET | Retrieves task lists from a Zoho Projects project. |
| [Update Task List](actions/update-task-list.md) | PUT | Updates an existing task list in Zoho Projects. |

### Issues

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | POST | Creates a new issue in Zoho Projects. |
| [Delete Issue](actions/delete-issue.md) | DELETE | Deletes an existing issue from Zoho Projects. |
| [Get Issue Details](actions/get-issue-details.md) | GET | Retrieves issue details from Zoho Projects. |
| [List Project Issues](actions/list-project-issues.md) | GET | Retrieves issues from a Zoho Projects project. |
| [Update Issue](actions/update-issue.md) | PUT | Updates an existing issue in Zoho Projects. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Zoho Projects. |
| [Get Project Details](actions/get-project-details.md) | GET | Retrieves project details from Zoho Projects. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from a Zoho Projects portal. |
| [Trash Project](actions/trash-project.md) | DELETE | Trashes an existing project in Zoho Projects. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Zoho Projects. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Zoho Projects. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Zoho Projects. |
| [Get Task Details](actions/get-task-details.md) | GET | Retrieves task details from Zoho Projects. |
| [List Tasks By Project](actions/list-tasks-by-project.md) | GET | Retrieves tasks from a Zoho Projects project. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Zoho Projects. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves user details from Zoho Projects. |
| [List Portal Users, Client Users, And Contacts](actions/list-portal-users-client-users-and-contacts.md) | GET | Retrieves portal users, client users, and contacts from Zoho Projects. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Portal Details](actions/get-portal-details.md) | GET | Retrieves portal details from Zoho Projects. |
| [List Portals](actions/list-portals.md) | GET | Retrieves portals from Zoho Projects. |

