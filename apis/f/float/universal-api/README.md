# <img src="https://images.mindcloud.co/apps/icons/symbol_1773773995073.png" alt="Float logo" width="28" height="28"> Float: Universal API

Schedule teams, manage projects, and track time

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/float/latest
- **Category:** Productivity / Scheduling
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.float.com
- **Vendor API docs:** https://developer.float.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List People](actions/list-people.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Float. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Float. |

### Milestone

| Action | Method | Description |
| --- | --- | --- |
| [Create Milestone](actions/create-milestone.md) | POST | Creates a new milestone in Float. |
| [List Milestones](actions/list-milestones.md) | GET | Retrieves milestones from Float. |

### People Report

| Action | Method | Description |
| --- | --- | --- |
| [Get People Report](actions/get-people-report.md) | GET | Retrieves a people report from Float. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a new person in Float. |
| [Get Person](actions/get-person.md) | GET | Retrieves person details from Float. |
| [List People](actions/list-people.md) | GET | Retrieves people from Float. |

### Phase

| Action | Method | Description |
| --- | --- | --- |
| [Create Phase](actions/create-phase.md) | POST | Creates a new phase in Float. |
| [List Phases](actions/list-phases.md) | GET | Retrieves phases from Float. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Float. |
| [Get Project](actions/get-project.md) | GET | Retrieves project details from Float. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Float. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Float. |

### Project Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Task](actions/create-project-task.md) | POST | Creates a new project task in Float. |
| [List Project Tasks](actions/list-project-tasks.md) | GET | Retrieves project tasks from Float. |

### Projects Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Projects Report](actions/get-projects-report.md) | GET | Retrieves a projects report from Float. |

### Resource Allocations

| Action | Method | Description |
| --- | --- | --- |
| [Create Allocation](actions/create-allocation.md) | POST | Creates a new allocation in Float. |
| [Get Allocation](actions/get-allocation.md) | GET | Retrieves allocation details from Float. |
| [List Allocations](actions/list-allocations.md) | GET | Retrieves allocations from Float. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from Float. |

### Time Off Requests

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Off](actions/create-time-off.md) | POST | Creates a new time off entry in Float. |
| [List Time Off](actions/list-time-off.md) | GET | Retrieves time off entries from Float. |

### Time Off Type

| Action | Method | Description |
| --- | --- | --- |
| [List Time Off Types](actions/list-time-off-types.md) | GET | Retrieves time off types from Float. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Create Logged Time](actions/create-logged-time.md) | POST | Creates a new logged time entry in Float. |
| [List Logged Time](actions/list-logged-time.md) | GET | Retrieves logged time entries from Float. |
| [Update Logged Time](actions/update-logged-time.md) | PUT | Updates an existing logged time entry in Float. |

