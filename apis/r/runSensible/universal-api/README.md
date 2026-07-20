# <img src="https://images.mindcloud.co/apps/icons/run-sensible-icon_1775574093427.png" alt="RunSensible logo" width="28" height="28"> RunSensible: Universal API

RunSensible is a legal practice management and CRM platform for leads, contacts, companies, opportunities, matters, tasks, appointments, tickets, quotes, invoices, notes, teams, dashboards, documents, and reports.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/runSensible/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 46
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.runsensible.com/
- **Vendor API docs:** https://help.runsensible.com/integration/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Contact](actions/get-contact.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=c6aaa7ff-ff5e-45fe-bc53-973062b499c9" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (46)

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | POST |  |
| [Delete Appointment](actions/delete-appointment.md) | DELETE |  |
| [Get Appointment](actions/get-appointment.md) | GET |  |
| [List Appointments](actions/list-appointments.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST |  |
| [Delete Company](actions/delete-company.md) | DELETE |  |
| [Get Company](actions/get-company.md) | GET |  |
| [Get Company Dashboard](actions/get-company-dashboard.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [Get Contact Dashboard](actions/get-contact-dashboard.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [Get Invoice Dashboard](actions/get-invoice-dashboard.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Convert Lead](actions/convert-lead.md) | PUT |  |
| [Create Lead](actions/create-lead.md) | POST |  |
| [Delete Lead](actions/delete-lead.md) | DELETE |  |
| [Get Lead](actions/get-lead.md) | GET |  |
| [Get Lead Dashboard](actions/get-lead-dashboard.md) | GET |  |
| [List Leads](actions/list-leads.md) | GET |  |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [List Notes](actions/list-notes.md) | GET |  |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Get Opportunity](actions/get-opportunity.md) | GET |  |
| [Get Opportunity Dashboard](actions/get-opportunity-dashboard.md) | GET |  |
| [List Opportunities](actions/list-opportunities.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Delete Project](actions/delete-project.md) | DELETE |  |
| [Get Project](actions/get-project.md) | GET |  |
| [Get Project Dashboard](actions/get-project-dashboard.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Quote](actions/get-quote.md) | GET |  |
| [Get Quote Dashboard](actions/get-quote-dashboard.md) | GET |  |
| [List Quotes](actions/list-quotes.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Complete Task](actions/complete-task.md) | PUT |  |
| [Create Task](actions/create-task.md) | POST |  |
| [Delete Task](actions/delete-task.md) | DELETE |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET |  |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST |  |
| [Delete Ticket](actions/delete-ticket.md) | DELETE |  |
| [Get Ticket](actions/get-ticket.md) | GET |  |
| [Get Ticket Dashboard](actions/get-ticket-dashboard.md) | GET |  |
| [List Tickets](actions/list-tickets.md) | GET |  |

