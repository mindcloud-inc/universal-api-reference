# RunSensible: Native API Reference

A consolidated summary of RunSensible's API configuration and 46 documented operations, with links to official documentation.

- **Official docs:** https://help.runsensible.com/integration/
- **API base URL:** `https://app.runsensible.com`

## Authentication

### API Key

RunSensible authenticates API requests with Authorization: Bearer <api_key>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.runsensible.com/integration/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `take` in the query string to set the page size (default 25; accepted range 1–200). Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Endpoints (46 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Complete Task](actions/complete-task.md) | `GET /api/Task/CompleteTask` | [docs](https://help.runsensible.com/integration/) |
| [Convert Lead](actions/convert-lead.md) | `POST /api/Lead/ConvertLeadToBusinessObjects` | [docs](https://help.runsensible.com/integration/) |
| [Create Appointment](actions/create-appointment.md) | `POST /api/Appointment/PostWithResult` | [docs](https://help.runsensible.com/integration/) |
| [Create Company](actions/create-company.md) | `POST /api/Company/PostWithResult` | [docs](https://help.runsensible.com/integration/) |
| [Create Contact](actions/create-contact.md) | `POST /api/Person/PostWithResult` | [docs](https://help.runsensible.com/integration/) |
| [Create Lead](actions/create-lead.md) | `POST /api/Lead/PostWithResult` | [docs](https://help.runsensible.com/integration/) |
| [Create Project](actions/create-project.md) | `POST /api/Project/PostWithResult` | [docs](https://help.runsensible.com/integration/) |
| [Create Task](actions/create-task.md) | `POST /api/Task/PostWithResult` | [docs](https://help.runsensible.com/integration/) |
| [Create Ticket](actions/create-ticket.md) | `POST /api/Ticket/PostWithResult` | [docs](https://help.runsensible.com/integration/) |
| [Delete Appointment](actions/delete-appointment.md) | `DELETE /api/Appointment/Delete` | [docs](https://help.runsensible.com/integration/) |
| [Delete Company](actions/delete-company.md) | `DELETE /api/Company/Delete` | [docs](https://help.runsensible.com/integration/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /api/Person/Delete` | [docs](https://help.runsensible.com/integration/) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /api/Lead/Delete` | [docs](https://help.runsensible.com/integration/) |
| [Delete Project](actions/delete-project.md) | `DELETE /api/Project/Delete` | [docs](https://help.runsensible.com/integration/) |
| [Delete Task](actions/delete-task.md) | `DELETE /api/Task/Delete` | [docs](https://help.runsensible.com/integration/) |
| [Delete Ticket](actions/delete-ticket.md) | `DELETE /api/Ticket/Delete` | [docs](https://help.runsensible.com/integration/) |
| [Get Appointment](actions/get-appointment.md) | `GET /api/Appointment/Get` | [docs](https://help.runsensible.com/integration/) |
| [Get Company](actions/get-company.md) | `GET /api/Company/Get` | [docs](https://help.runsensible.com/integration/) |
| [Get Company Dashboard](actions/get-company-dashboard.md) | `GET /api/Report/GetCompanyDashboard` | [docs](https://help.runsensible.com/integration/) |
| [Get Contact](actions/get-contact.md) | `GET /api/Person/Get` | [docs](https://help.runsensible.com/integration/) |
| [Get Contact Dashboard](actions/get-contact-dashboard.md) | `GET /api/Report/GetPersonDashboard` | [docs](https://help.runsensible.com/integration/) |
| [Get Invoice](actions/get-invoice.md) | `GET /api/invoice/Get` | [docs](https://help.runsensible.com/integration/) |
| [Get Invoice Dashboard](actions/get-invoice-dashboard.md) | `GET /api/Report/GetInvoiceDashboard` | [docs](https://help.runsensible.com/integration/) |
| [Get Lead](actions/get-lead.md) | `GET /api/Lead/Get` | [docs](https://help.runsensible.com/integration/) |
| [Get Lead Dashboard](actions/get-lead-dashboard.md) | `GET /api/Report/GetLeadDashboard` | [docs](https://help.runsensible.com/integration/) |
| [Get Opportunity](actions/get-opportunity.md) | `GET /api/opportunity/Get` | [docs](https://help.runsensible.com/integration/) |
| [Get Opportunity Dashboard](actions/get-opportunity-dashboard.md) | `GET /api/Report/GetOpportunityDashboard` | [docs](https://help.runsensible.com/integration/) |
| [Get Project](actions/get-project.md) | `GET /api/Project/Get` | [docs](https://help.runsensible.com/integration/) |
| [Get Project Dashboard](actions/get-project-dashboard.md) | `GET /api/Report/GetProjectDashboard` | [docs](https://help.runsensible.com/integration/) |
| [Get Quote](actions/get-quote.md) | `GET /api/quote/Get` | [docs](https://help.runsensible.com/integration/) |
| [Get Quote Dashboard](actions/get-quote-dashboard.md) | `GET /api/Report/GetQuoteDashboard` | [docs](https://help.runsensible.com/integration/) |
| [Get Task](actions/get-task.md) | `GET /api/Task/Get` | [docs](https://help.runsensible.com/integration/) |
| [Get Ticket](actions/get-ticket.md) | `GET /api/Ticket/Get` | [docs](https://help.runsensible.com/integration/) |
| [Get Ticket Dashboard](actions/get-ticket-dashboard.md) | `GET /api/Report/GetTicketDashboard` | [docs](https://help.runsensible.com/integration/) |
| [List Appointments](actions/list-appointments.md) | `GET /api/Appointment/GetAllPaged` | [docs](https://help.runsensible.com/integration/) |
| [List Companies](actions/list-companies.md) | `GET /api/Company/GetAllPaged` | [docs](https://help.runsensible.com/integration/) |
| [List Contacts](actions/list-contacts.md) | `GET /api/Person/GetAllPaged` | [docs](https://help.runsensible.com/integration/) |
| [List Invoices](actions/list-invoices.md) | `GET /api/invoice/GetAllPaged` | [docs](https://help.runsensible.com/integration/) |
| [List Leads](actions/list-leads.md) | `GET /api/Lead/GetAllPaged` | [docs](https://help.runsensible.com/integration/) |
| [List Notes](actions/list-notes.md) | `GET /api/note/GetAllPaged` | [docs](https://help.runsensible.com/integration/) |
| [List Opportunities](actions/list-opportunities.md) | `GET /api/opportunity/GetAllPaged` | [docs](https://help.runsensible.com/integration/) |
| [List Projects](actions/list-projects.md) | `GET /api/Project/GetAllPaged` | [docs](https://help.runsensible.com/integration/) |
| [List Quotes](actions/list-quotes.md) | `GET /api/quote/GetAllPaged` | [docs](https://help.runsensible.com/integration/) |
| [List Tasks](actions/list-tasks.md) | `GET /api/Task/GetAllPaged` | [docs](https://help.runsensible.com/integration/) |
| [List Teams](actions/list-teams.md) | `GET /api/Team/GetAllPaged` | [docs](https://help.runsensible.com/integration/) |
| [List Tickets](actions/list-tickets.md) | `GET /api/Ticket/GetAllPaged` | [docs](https://help.runsensible.com/integration/) |
