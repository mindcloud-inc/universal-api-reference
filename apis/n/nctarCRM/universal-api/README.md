# <img src="https://images.mindcloud.co/apps/icons/favicon-nectar_1776269455952.png" alt="Néctar CRM logo" width="28" height="28"> Néctar CRM: Universal API

Manage contacts, opportunities, tasks, and CRM workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nctarCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nectarcrm.com.br
- **Vendor API docs:** https://nectarcrm.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nctarCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Calendar Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | POST | Creates a new appointment in Néctar CRM. |
| [Get Appointment](actions/get-appointment.md) | GET | Retrieves an appointment from Néctar CRM. |
| [List Appointments](actions/list-appointments.md) | GET | Retrieves appointments from Néctar CRM. |
| [Update Appointment](actions/update-appointment.md) | PUT | Updates an existing appointment in Néctar CRM. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Néctar CRM. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Néctar CRM. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Néctar CRM. |
| [Search Contacts by Email](actions/search-contacts-by-email.md) | GET | Finds contacts in Néctar CRM by email address. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Néctar CRM. |

### Opportunities

| Action | Method | Description |
| --- | --- | --- |
| [List Opportunities](actions/list-opportunities.md) | GET | Retrieves opportunities from Néctar CRM. |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from Néctar CRM. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves products from Néctar CRM. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from Néctar CRM. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Néctar CRM. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Néctar CRM. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Néctar CRM. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Néctar CRM. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Néctar CRM. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Origins](actions/list-origins.md) | GET | Retrieves origins from Néctar CRM. |
| [List Qualifications](actions/list-qualifications.md) | GET | Retrieves qualifications from Néctar CRM. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Néctar CRM. |

