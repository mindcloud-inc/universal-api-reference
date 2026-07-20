# <img src="https://images.mindcloud.co/apps/icons/beebole_1774295382028.png" alt="Beebole logo" width="28" height="28"> Beebole: Universal API

Track project time, manage approvals, and analyze costs and billing

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/beebole/latest
- **Category:** Human Resources / HRIS
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://beebole.com
- **Vendor API docs:** https://beebole.com/help/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Companies](actions/list-companies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Activate a Company](actions/activate-a-company.md) | PUT | Activates a company in Beebole. |
| [Create a Company](actions/create-a-company.md) | POST | Creates a new company in Beebole. |
| [Deactivate a Company](actions/deactivate-a-company.md) | PUT | Deactivates a company in Beebole. |
| [Get a Company](actions/get-a-company.md) | GET | Retrieves a company from your Beebole account. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from your Beebole account. |
| [Update a Company](actions/update-a-company.md) | PUT | Updates an existing company in Beebole. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Activate a Person](actions/activate-a-person.md) | PUT | Activates a person in Beebole. |
| [Create a Person](actions/create-a-person.md) | POST | Creates a new person in Beebole. |
| [Deactivate a Person](actions/deactivate-a-person.md) | PUT | Deactivates a person in Beebole. |
| [Get a Person](actions/get-a-person.md) | GET | Retrieves a person from your Beebole account. |
| [List Persons](actions/list-persons.md) | GET | Retrieves people from your Beebole account. |
| [Update a Person](actions/update-a-person.md) | PUT | Updates an existing person in Beebole. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Activate a Project](actions/activate-a-project.md) | PUT | Activates a project in Beebole. |
| [Create a Project](actions/create-a-project.md) | POST | Creates a new project in Beebole. |
| [Deactivate a Project](actions/deactivate-a-project.md) | PUT | Deactivates a project in Beebole. |
| [Get a Project](actions/get-a-project.md) | GET | Retrieves a project from your Beebole account. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from your Beebole account. |
| [Update a Project](actions/update-a-project.md) | PUT | Updates an existing project in Beebole. |

### Subproject

| Action | Method | Description |
| --- | --- | --- |
| [Activate a Subproject](actions/activate-a-subproject.md) | PUT | Activates a subproject in Beebole. |
| [Create a Subproject](actions/create-a-subproject.md) | POST | Creates a new subproject in Beebole. |
| [Deactivate a Subproject](actions/deactivate-a-subproject.md) | PUT | Deactivates a subproject in Beebole. |
| [Get a Subproject](actions/get-a-subproject.md) | GET | Retrieves a subproject from your Beebole account. |
| [List Subprojects](actions/list-subprojects.md) | GET | Retrieves subprojects from your Beebole account. |
| [Update a Subproject](actions/update-a-subproject.md) | PUT | Updates an existing subproject in Beebole. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Activate a Task](actions/activate-a-task.md) | PUT | Activates a task in Beebole. |
| [Create a Task](actions/create-a-task.md) | POST | Creates a new task in Beebole. |
| [Deactivate a Task](actions/deactivate-a-task.md) | PUT | Deactivates a task in Beebole. |
| [Get a Task](actions/get-a-task.md) | GET | Retrieves a task from your Beebole account. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from your Beebole account. |
| [Update a Task](actions/update-a-task.md) | PUT | Updates an existing task in Beebole. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Approve Time Entry](actions/approve-time-entry.md) | PUT | Approves a time entry in Beebole. |
| [Create a Time Entry](actions/create-a-time-entry.md) | POST | Creates a new time entry in Beebole. |
| [Delete a Time Entry](actions/delete-a-time-entry.md) | DELETE | Deletes an existing time entry from Beebole. |
| [Get a Time Entry](actions/get-a-time-entry.md) | GET | Retrieves a time entry from your Beebole account. |
| [Get Tasks to Create a Time Entry](actions/get-tasks-to-create-a-time-entry.md) | GET | Retrieves tasks for creating a time entry in Beebole. |
| [Get Time Entry Entities](actions/get-time-entry-entities.md) | GET | Retrieves available entities for a time entry in Beebole. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from your Beebole account. |
| [Reject Time Entry](actions/reject-time-entry.md) | PUT | Rejects a time entry in Beebole. |
| [Submit Time Entry](actions/submit-time-entry.md) | PUT | Submits a time entry for approval in Beebole. |
| [Update a Time Entry](actions/update-a-time-entry.md) | PUT | Updates an existing time entry in Beebole. |

