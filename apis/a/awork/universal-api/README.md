# <img src="https://images.mindcloud.co/apps/icons/awork_1774056293307.png" alt="Awork logo" width="28" height="28"> Awork: Universal API

Work management platform for projects, tasks, users, companies, documents, time tracking, and workload planning.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/awork/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.awork.com/
- **Vendor API docs:** https://developers.awork.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/awork/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Comment](actions/create-task-comment.md) | POST | Creates a task comment in Awork. |
| [List Task Comments](actions/list-task-comments.md) | GET | Retrieves task comments from Awork. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from Awork. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Awork. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Awork. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Awork. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a project in Awork. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Awork. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Awork. |
| [Update Project](actions/update-project.md) | PUT | Updates a project in Awork. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Workspace](actions/search-workspace.md) | GET | Finds workspace entities in Awork by search term. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a task in Awork. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Awork. |
| [Get Task By Key](actions/get-task-by-key.md) | GET | Retrieves a task from Awork by key. |
| [List Assigned Tasks](actions/list-assigned-tasks.md) | GET | Retrieves assigned tasks from Awork. |
| [List Project Tasks](actions/list-project-tasks.md) | GET | Retrieves project tasks from Awork. |
| [Set Task Assignees](actions/set-task-assignees.md) | PUT | Updates task assignees in Awork. |
| [Update Task](actions/update-task.md) | PUT | Updates a task in Awork. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a time entry in Awork using UTC start values. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from Awork. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Awork. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Awork. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Awork. |

### Workload

| Action | Method | Description |
| --- | --- | --- |
| [List User Workloads](actions/list-user-workloads.md) | GET | Retrieves user workloads from Awork. |

