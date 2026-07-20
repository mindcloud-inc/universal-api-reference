# <img src="https://images.mindcloud.co/apps/icons/nutshell_1773351505459.png" alt="Nutshell logo" width="28" height="28"> Nutshell: Universal API

CRM for managing leads, contacts, companies, tasks, activities, notes, and related sales workflows in Nutshell.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nutshell/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nutshell.com
- **Vendor API docs:** https://developers.nutshell.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Leads](actions/list-leads.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/list-leads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from Nutshell. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Nutshell. |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from Nutshell. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Nutshell. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Nutshell. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Nutshell. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Nutshell. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Nutshell. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Nutshell. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Nutshell. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from Nutshell. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from Nutshell. |
| [Reopen Lead](actions/reopen-lead.md) | PUT | Reopens a closed lead in Nutshell. |
| [Set Lead Pipeline](actions/set-lead-pipeline.md) | PUT | Updates a lead's pipeline in Nutshell. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Nutshell. |
| [Update Lead Status](actions/update-lead-status.md) | PUT | Updates a lead's status in Nutshell. |

### Lead Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Stages](actions/list-lead-stages.md) | GET | Retrieves a lead's stages from Nutshell. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note in Nutshell. |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from Nutshell. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Nutshell. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Nutshell. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Nutshell. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Nutshell. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Nutshell. |

