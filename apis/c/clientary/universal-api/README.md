# <img src="https://images.mindcloud.co/apps/icons/clientary_1774368943954.png" alt="Clientary logo" width="28" height="28"> Clientary: Universal API

Manage client projects, proposals, invoices, payments, and time tracking

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clientary/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.clientary.com/
- **Vendor API docs:** https://www.clientary.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Clients](actions/list-clients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Clientary. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Clientary by client ID. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from your Clientary account. |
| [Update Client](actions/update-client.md) | PUT | Updates a client in Clientary by client ID. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact for a client in Clientary. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Clientary by contact ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from your Clientary account. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in Clientary by contact ID. |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST | Creates a new estimate in Clientary. |
| [Get Estimate](actions/get-estimate.md) | GET | Retrieves an estimate from Clientary by estimate ID. |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves estimates from your Clientary account. |
| [Update Estimate](actions/update-estimate.md) | PUT | Updates an estimate in Clientary by estimate ID. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Clientary. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Clientary by invoice ID. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from your Clientary account. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an invoice in Clientary by invoice ID. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Clientary. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Clientary by project ID. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from your Clientary account. |
| [Update Project](actions/update-project.md) | PUT | Updates a project in Clientary by project ID. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Clientary. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Clientary by task ID. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from your Clientary account. |
| [Update Task](actions/update-task.md) | PUT | Updates a task in Clientary by task ID. |

