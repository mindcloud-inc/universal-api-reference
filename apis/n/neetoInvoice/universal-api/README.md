# <img src="https://images.mindcloud.co/apps/icons/neeto-invoice_1775485944066.png" alt="NeetoInvoice logo" width="28" height="28"> NeetoInvoice: Universal API

NeetoInvoice API integration for managing clients, recipients, projects, project users, team members, time entries, and invoice generation in NeetoInvoice workspaces.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/neetoInvoice/latest
- **Category:** Commerce / Accounting
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.neeto.com/neetoinvoice
- **Vendor API docs:** https://apidocs.neetoinvoice.com/getting-started/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Team Members](actions/list-team-members.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/list-team-members?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipient](actions/create-recipient.md) | POST | Creates a new recipient in NeetoInvoice. |
| [Delete Recipient](actions/delete-recipient.md) | DELETE | Deletes an existing recipient from NeetoInvoice. |
| [Update Recipient](actions/update-recipient.md) | PUT | Updates an existing recipient in NeetoInvoice. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in NeetoInvoice. |
| [Get Client](actions/get-client.md) | GET | Retrieves details for a client from NeetoInvoice. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in NeetoInvoice. |
| [Update Client Status](actions/update-client-status.md) | PUT | Updates a client status in NeetoInvoice. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Generate Invoice](actions/generate-invoice.md) | POST | Generates an invoice for a client in NeetoInvoice. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Add Project User](actions/add-project-user.md) | POST | Adds a user to a project in NeetoInvoice. |
| [List Project Users](actions/list-project-users.md) | GET | Retrieves all project users from NeetoInvoice. |
| [Remove Project User](actions/remove-project-user.md) | DELETE | Removes a user from a project in NeetoInvoice. |
| [Update Project User](actions/update-project-user.md) | PUT | Updates a project user in NeetoInvoice. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in NeetoInvoice. |
| [Get Project](actions/get-project.md) | GET | Retrieves details for a project from NeetoInvoice. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in NeetoInvoice. |
| [Update Project Status](actions/update-project-status.md) | PUT | Updates a project status in NeetoInvoice. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in NeetoInvoice. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves unbilled time entries from NeetoInvoice. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add Team Members](actions/add-team-members.md) | POST | Adds new team members in NeetoInvoice. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves all team members from NeetoInvoice. |
| [Remove Team Members](actions/remove-team-members.md) | DELETE | Removes selected team members from NeetoInvoice. |
| [Update Team Member](actions/update-team-member.md) | PUT | Updates an existing team member in NeetoInvoice. |

