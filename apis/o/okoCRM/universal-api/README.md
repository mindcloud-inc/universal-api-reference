# <img src="https://images.mindcloud.co/apps/icons/favicon-okocrm-com-48x48_1776947283635.png" alt="OkoCRM logo" width="28" height="28"> OkoCRM: Universal API

Connect OkoCRM to read and manage users, contacts, companies, deals, tasks, notes, pipelines, fields, and supporting CRM reference data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/okoCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://okocrm.com/
- **Vendor API docs:** https://okocrm.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create company](actions/create-company.md) | POST | Creates a new company in OkoCRM. |
| [Delete company](actions/delete-company.md) | DELETE | Deletes an existing company from OkoCRM. |
| [Get company](actions/get-company.md) | GET | Retrieves company details from OkoCRM. |
| [Link company entities](actions/link-company-entities.md) | PUT | Links entities to a company in OkoCRM. |
| [List companies](actions/list-companies.md) | GET | Retrieves companies from OkoCRM. |
| [Update company](actions/update-company.md) | PUT | Updates an existing company in OkoCRM. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create contact](actions/create-contact.md) | POST | Creates a new contact in OkoCRM. |
| [Delete contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from OkoCRM. |
| [Get contact](actions/get-contact.md) | GET | Retrieves contact details from OkoCRM. |
| [Link contact entities](actions/link-contact-entities.md) | PUT | Links entities to a contact in OkoCRM. |
| [List contacts](actions/list-contacts.md) | GET | Retrieves contacts from OkoCRM. |
| [Update contact](actions/update-contact.md) | PUT | Updates an existing contact in OkoCRM. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List fields](actions/list-fields.md) | GET | Retrieves custom fields from OkoCRM. |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Create deal](actions/create-deal.md) | POST | Creates a new deal in OkoCRM. |
| [Delete deal](actions/delete-deal.md) | DELETE | Deletes an existing deal from OkoCRM. |
| [Get deal](actions/get-deal.md) | GET | Retrieves deal details from OkoCRM. |
| [Link deal entities](actions/link-deal-entities.md) | PUT | Links entities to a deal in OkoCRM. |
| [List deals](actions/list-deals.md) | GET | Retrieves deals from OkoCRM. |
| [Update deal](actions/update-deal.md) | PUT | Updates an existing deal in OkoCRM. |

### Engagement Types

| Action | Method | Description |
| --- | --- | --- |
| [List task types](actions/list-task-types.md) | GET | Retrieves task types from OkoCRM. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List cities](actions/list-cities.md) | GET | Retrieves cities from OkoCRM. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create note](actions/create-note.md) | POST | Creates a new note in OkoCRM. |
| [List notes](actions/list-notes.md) | GET | Retrieves notes from OkoCRM. |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [List pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from OkoCRM. |

### Stages

| Action | Method | Description |
| --- | --- | --- |
| [List pipeline stages](actions/list-pipeline-stages.md) | GET | Retrieves pipeline stages for a pipeline in OkoCRM. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Complete task with comment](actions/complete-task-with-comment.md) | PUT | Marks a task as done in OkoCRM with a comment. |
| [Create task](actions/create-task.md) | POST | Creates a new task in OkoCRM. |
| [Delete task](actions/delete-task.md) | DELETE | Deletes an existing task from OkoCRM. |
| [List tasks](actions/list-tasks.md) | GET | Retrieves tasks from OkoCRM. |
| [Update task](actions/update-task.md) | PUT | Updates an existing task in OkoCRM. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List users](actions/list-users.md) | GET | Retrieves users from OkoCRM. |

