# <img src="https://images.mindcloud.co/apps/icons/moxie_1773435825019.png" alt="Moxie logo" width="28" height="28"> Moxie: Universal API

Manage clients, projects, invoices, and payments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moxie/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.withmoxie.com
- **Vendor API docs:** https://help.withmoxie.com/en/collections/5482062-public-api-endpoints

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspace Users](actions/list-workspace-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/list-workspace-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Moxie. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Moxie. |
| [Search Clients](actions/search-clients.md) | GET | Finds clients in Moxie. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Moxie. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Moxie. |

### Email Template

| Action | Method | Description |
| --- | --- | --- |
| [List Email Templates](actions/list-email-templates.md) | GET | Retrieves email templates from Moxie. |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | POST | Creates a new expense in Moxie. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Form Names](actions/list-form-names.md) | GET | Retrieves form names from Moxie. |

### Form Submission

| Action | Method | Description |
| --- | --- | --- |
| [Create Form Submission](actions/create-form-submission.md) | POST | Creates a new form submission in Moxie. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Moxie. |

### Invoice Payment

| Action | Method | Description |
| --- | --- | --- |
| [Apply Payment to Invoice](actions/apply-payment-to-invoice.md) | POST | Applies a payment to an invoice in Moxie. |

### Invoice Template

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Templates](actions/list-invoice-templates.md) | GET | Retrieves invoice templates from Moxie. |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity](actions/create-opportunity.md) | POST | Creates a new opportunity in Moxie. |

### Payable Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Search Payable Invoices](actions/search-payable-invoices.md) | GET | Finds payable invoices in Moxie. |

### Pipeline Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Pipeline Stages](actions/list-pipeline-stages.md) | GET | Retrieves pipeline stages from Moxie. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Moxie. |
| [Search Projects](actions/search-projects.md) | GET | Finds projects in Moxie. |

### Project Task Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Project Task Stages](actions/list-project-task-stages.md) | GET | Retrieves project task stages from Moxie. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Moxie. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in Moxie. |

### Ticket Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment on Ticket](actions/create-comment-on-ticket.md) | POST | Creates a comment on a ticket in Moxie. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in Moxie. |

### Vendor

| Action | Method | Description |
| --- | --- | --- |
| [List Vendor Names](actions/list-vendor-names.md) | GET | Retrieves vendor names from Moxie. |

### Workspace User

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Users](actions/list-workspace-users.md) | GET | Retrieves workspace users from Moxie. |

