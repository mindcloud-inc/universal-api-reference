# <img src="https://images.mindcloud.co/apps/icons/6fa34b0d-b1b7-41ce-9d15-9f7c600dd818-medium_1775672790418.jpeg" alt="Datalyse logo" width="28" height="28"> Datalyse: Universal API

Datalyse CRM and sales operations wrapper for leads, companies, opportunities, tasks, tickets, invoices, and email workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/datalyse/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.datalyse.io
- **Vendor API docs:** https://developers.datalyse.io/devs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get All Agents](actions/get-all-agents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/get-all-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Get All Agents](actions/get-all-agents.md) | GET | Retrieves all company agents from Datalyse. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Add Note To Company](actions/add-note-to-company.md) | PUT | Adds a note to a company in Datalyse. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from Datalyse. |
| [Edit Company](actions/edit-company.md) | PUT | Updates an existing company in Datalyse. |
| [Get Companies](actions/get-companies.md) | GET | Retrieves a list of companies from Datalyse. |
| [Get Company Activity](actions/get-company-activity.md) | GET | Retrieves activity for a company from Datalyse. |

### Company Context

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Types](actions/get-agent-types.md) | GET | Retrieves company agent types from Datalyse. |
| [Get Company Properties](actions/get-company-properties.md) | GET | Retrieves company properties and statuses from Datalyse. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Get Email](actions/get-email.md) | GET | Retrieves a single email from Datalyse. |
| [Get Emails](actions/get-emails.md) | GET | Retrieves emails from Datalyse by folder. |
| [Send Email](actions/send-email.md) | POST | Sends an email from Datalyse. |

### Email Signature

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Signatures](actions/get-email-signatures.md) | GET | Retrieves all email signatures from Datalyse. |

### Email Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Template](actions/create-email-template.md) | POST | Creates a new email template in Datalyse. |
| [Delete Email Template](actions/delete-email-template.md) | DELETE | Deletes an existing email template from Datalyse. |
| [Edit Email Template](actions/edit-email-template.md) | PUT | Updates an existing email template in Datalyse. |
| [Get Email Templates](actions/get-email-templates.md) | GET | Retrieves all email templates from Datalyse. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoices](actions/get-invoices.md) | GET | Retrieves invoices for the authenticated agent from Datalyse. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Add Note To Lead](actions/add-note-to-lead.md) | PUT | Adds a note to a contact or company in Datalyse. |
| [Create Lead](actions/create-lead.md) | POST | Creates a new contact or company in Datalyse. |
| [Delete Lead](actions/delete-lead.md) | DELETE | Deletes an existing contact or company from Datalyse. |
| [Edit Lead](actions/edit-lead.md) | PUT | Updates an existing contact or company in Datalyse. |
| [Get Lead Activity](actions/get-lead-activity.md) | GET | Retrieves activity for a contact from Datalyse. |
| [Get Leads](actions/get-leads.md) | GET | Retrieves contacts or companies from Datalyse. |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Add Note To Opportunity](actions/add-note-to-opportunity.md) | PUT | Adds a note to an opportunity in Datalyse. |
| [Create Opportunity](actions/create-opportunity.md) | POST | Creates a new opportunity in Datalyse. |
| [Delete Opportunity](actions/delete-opportunity.md) | DELETE | Deletes an existing opportunity from Datalyse. |
| [Edit Opportunity](actions/edit-opportunity.md) | PUT | Updates an existing opportunity in Datalyse. |
| [Get Opportunities](actions/get-opportunities.md) | GET | Retrieves a list of opportunities from Datalyse. |
| [Get Opportunity Activity](actions/get-opportunity-activity.md) | GET | Retrieves activity for an opportunity from Datalyse. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Add Note To Task](actions/add-note-to-task.md) | PUT | Adds a note to a task in Datalyse. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Datalyse. |
| [Edit Task](actions/edit-task.md) | PUT | Updates an existing task in Datalyse. |
| [Get Task Activity](actions/get-task-activity.md) | GET | Retrieves activity for a task from Datalyse. |
| [Get Tasks](actions/get-tasks.md) | GET | Retrieves a list of tasks from Datalyse. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Add Note To Ticket](actions/add-note-to-ticket.md) | PUT | Adds a note to a ticket in Datalyse. |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in Datalyse. |
| [Delete Ticket](actions/delete-ticket.md) | DELETE | Deletes an existing ticket from Datalyse. |
| [Edit Ticket](actions/edit-ticket.md) | PUT | Updates an existing ticket in Datalyse. |
| [Get Ticket Activity](actions/get-ticket-activity.md) | GET | Retrieves activity for a ticket from Datalyse. |
| [Get Tickets](actions/get-tickets.md) | GET | Retrieves a list of tickets from Datalyse. |

