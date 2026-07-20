# <img src="https://images.mindcloud.co/apps/icons/outlign_1776096732775.png" alt="Outlign logo" width="28" height="28"> Outlign: Universal API

Manage projects, clients, tasks, and milestones

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/outlign/latest
- **Category:** Productivity / Project Management
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://outlign.co
- **Vendor API docs:** https://go.outlign.co/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlign/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Outlign. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from Outlign. |
| [Get Client](actions/get-client.md) | GET | Retrieves a specific client from Outlign. |
| [List Clients](actions/list-clients.md) | GET | Retrieves accessible client records from Outlign. |
| [List Clients By Company](actions/list-clients-by-company.md) | GET | Retrieves client records from Outlign by company. |
| [Search Clients By Title](actions/search-clients-by-title.md) | GET | Finds clients in Outlign by title. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Outlign. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET | Retrieves accessible company records from Outlign. |

### Milestone

| Action | Method | Description |
| --- | --- | --- |
| [List Milestones](actions/list-milestones.md) | GET | Retrieves accessible milestone records from Outlign. |

### Phase

| Action | Method | Description |
| --- | --- | --- |
| [Create Internal Phase](actions/create-internal-phase.md) | POST | Creates a new internal phase in Outlign. |
| [Create Phase](actions/create-phase.md) | POST | Creates a new client-facing phase in Outlign. |
| [Get Phase](actions/get-phase.md) | GET | Retrieves a specific phase from Outlign. |
| [List Client-Facing Phases](actions/list-client-facing-phases.md) | GET | Retrieves client-facing phase records from Outlign. |
| [List Internal Phases](actions/list-internal-phases.md) | GET | Retrieves internal phase records from Outlign. |
| [List Phases](actions/list-phases.md) | GET | Retrieves project phase records from Outlign. |
| [List Phases By Client](actions/list-phases-by-client.md) | GET | Retrieves project phase records from Outlign by client. |
| [List Phases By Company](actions/list-phases-by-company.md) | GET | Retrieves project phase records from Outlign by company. |
| [List Phases By Project](actions/list-phases-by-project.md) | GET | Retrieves project phase records from Outlign by project. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a specific project from Outlign. |
| [List Projects](actions/list-projects.md) | GET | Retrieves accessible project records from Outlign. |
| [List Projects By Client](actions/list-projects-by-client.md) | GET | Retrieves project records from Outlign by client. |
| [List Projects By Company](actions/list-projects-by-company.md) | GET | Retrieves project records from Outlign by company. |
| [Search Projects By Title](actions/search-projects-by-title.md) | GET | Finds projects in Outlign by title. |

### Project Template

| Action | Method | Description |
| --- | --- | --- |
| [List Project Templates](actions/list-project-templates.md) | GET | Retrieves available project templates from Outlign. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Outlign. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Outlign. |
| [Get Task](actions/get-task.md) | GET | Retrieves a specific task from Outlign. |
| [List Completed Tasks](actions/list-completed-tasks.md) | GET | Retrieves completed task records from Outlign. |
| [List Non-Template Tasks](actions/list-non-template-tasks.md) | GET | Retrieves non-template task records from Outlign. |
| [List Open Tasks](actions/list-open-tasks.md) | GET | Retrieves open task records from Outlign. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves accessible task records from Outlign. |
| [List Tasks With Due Dates](actions/list-tasks-with-due-dates.md) | GET | Retrieves task records with due dates from Outlign. |
| [Mark Task Completed](actions/mark-task-completed.md) | PUT | Updates an existing task to completed in Outlign. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Outlign. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current authenticated user from Outlign. |

