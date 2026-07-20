# Datalyse: Native API Reference

A consolidated summary of Datalyse's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.datalyse.io/devs/
- **API base URL:** `https://api.datalyse.io`

## Authentication

### API Token

Use a Datalyse API token generated for the target account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.datalyse.io/devs/content_api.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Note To Company](actions/add-note-to-company.md) | `POST /api/1.0/companies/addnote.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Add Note To Lead](actions/add-note-to-lead.md) | `POST /api/1.0/leads/addnote.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Add Note To Opportunity](actions/add-note-to-opportunity.md) | `POST /api/1.0/opportunities/addnote.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Add Note To Task](actions/add-note-to-task.md) | `POST /api/1.0/tasks/addnote.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Add Note To Ticket](actions/add-note-to-ticket.md) | `POST /api/1.0/tickets/addnote.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Create Email Template](actions/create-email-template.md) | `POST /api/1.0/emails/templates/create.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Create Lead](actions/create-lead.md) | `POST /api/1.0/leads/create.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Create Opportunity](actions/create-opportunity.md) | `POST /api/1.0/opportunities/create.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Create Ticket](actions/create-ticket.md) | `POST /api/1.0/tickets/create.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Delete Company](actions/delete-company.md) | `POST /api/1.0/companies/delete.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Delete Email Template](actions/delete-email-template.md) | `POST /api/1.0/emails/templates/delete.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Delete Lead](actions/delete-lead.md) | `POST /api/1.0/leads/delete.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Delete Opportunity](actions/delete-opportunity.md) | `POST /api/1.0/opportunities/delete.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Delete Task](actions/delete-task.md) | `POST /api/1.0/tasks/delete.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Delete Ticket](actions/delete-ticket.md) | `POST /api/1.0/tickets/delete.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Edit Company](actions/edit-company.md) | `POST /api/1.0/companies/edit.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Edit Email Template](actions/edit-email-template.md) | `POST /api/1.0/emails/templates/edit.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Edit Lead](actions/edit-lead.md) | `POST /api/1.0/leads/edit.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Edit Opportunity](actions/edit-opportunity.md) | `POST /api/1.0/opportunities/edit.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Edit Task](actions/edit-task.md) | `POST /api/1.0/tasks/edit.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Edit Ticket](actions/edit-ticket.md) | `POST /api/1.0/tickets/edit.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Agent Types](actions/get-agent-types.md) | `POST /api/1.0/companyuserdata/agentstypes.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get All Agents](actions/get-all-agents.md) | `POST /api/1.0/companyuserdata/getallagents.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Companies](actions/get-companies.md) | `POST /api/1.0/companies/get.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Company Activity](actions/get-company-activity.md) | `POST /api/1.0/companies/getactivity.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Company Properties](actions/get-company-properties.md) | `POST /api/1.0/companyuserdata/companyproperties.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Email](actions/get-email.md) | `POST /api/1.0/emails/getone.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Email Signatures](actions/get-email-signatures.md) | `POST /api/1.0/emails/signatures/get.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Email Templates](actions/get-email-templates.md) | `POST /api/1.0/emails/templates/get.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Emails](actions/get-emails.md) | `POST /api/1.0/emails/get.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Invoices](actions/get-invoices.md) | `POST /api/1.0/companyuserdata/invoicesget.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Lead Activity](actions/get-lead-activity.md) | `POST /api/1.0/leads/getactivity.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Leads](actions/get-leads.md) | `POST /api/1.0/leads/get.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Opportunities](actions/get-opportunities.md) | `POST /api/1.0/opportunities/get.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Opportunity Activity](actions/get-opportunity-activity.md) | `POST /api/1.0/opportunities/getactivity.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Task Activity](actions/get-task-activity.md) | `POST /api/1.0/tasks/getactivity.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Tasks](actions/get-tasks.md) | `POST /api/1.0/tasks/get.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Ticket Activity](actions/get-ticket-activity.md) | `POST /api/1.0/tickets/getactivity.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Get Tickets](actions/get-tickets.md) | `POST /api/1.0/tickets/get.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
| [Send Email](actions/send-email.md) | `POST /api/1.0/emails/send.json` | [docs](https://developers.datalyse.io/devs/content_api.html) |
