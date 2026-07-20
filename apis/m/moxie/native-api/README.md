# Moxie: Native API Reference

A consolidated summary of Moxie's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://help.withmoxie.com/en/collections/5482062-public-api-endpoints
- **API base URL:** `https://pod01.withmoxie.com/api/public`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.withmoxie.com/en/articles/8154735-public-api-fundamentals)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Payment to Invoice](actions/apply-payment-to-invoice.md) | `POST /action/payment/create` | [docs](https://help.withmoxie.com/en/articles/8213724-apply-payment-to-invoice) |
| [Create Client](actions/create-client.md) | `POST /action/clients/create` | [docs](https://help.withmoxie.com/en/articles/8160175-create-client) |
| [Create Comment on Ticket](actions/create-comment-on-ticket.md) | `POST /action/tickets/comments/create` | [docs](https://help.withmoxie.com/en/articles/9367926-create-comment-on-ticket) |
| [Create Contact](actions/create-contact.md) | `POST /action/contacts/create` | [docs](https://help.withmoxie.com/en/articles/8160213-create-contact) |
| [Create Expense](actions/create-expense.md) | `POST /action/expenses/create` | [docs](https://help.withmoxie.com/en/articles/8160223-create-expense) |
| [Create Form Submission](actions/create-form-submission.md) | `POST /action/formSubmissions/create` | [docs](https://help.withmoxie.com/en/articles/8160298-create-form-submission) |
| [Create Invoice](actions/create-invoice.md) | `POST /action/invoices/create` | [docs](https://help.withmoxie.com/en/articles/8174518-create-invoice) |
| [Create Opportunity](actions/create-opportunity.md) | `POST /action/opportunities/create` | [docs](https://help.withmoxie.com/en/articles/8160471-create-opportunity) |
| [Create Project](actions/create-project.md) | `POST /action/projects/create` | [docs](https://help.withmoxie.com/en/articles/8160400-create-project) |
| [Create Task](actions/create-task.md) | `POST /action/tasks/create` | [docs](https://help.withmoxie.com/en/articles/8160423-create-task) |
| [Create Ticket](actions/create-ticket.md) | `POST /action/tickets/create` | [docs](https://help.withmoxie.com/en/articles/9367715-create-ticket) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /action/timeWorked/create` | [docs](https://help.withmoxie.com/en/articles/8160498-create-time-entry) |
| [List Clients](actions/list-clients.md) | `GET /action/clients/list` | [docs](https://help.withmoxie.com/en/articles/8163927-list-clients) |
| [List Email Templates](actions/list-email-templates.md) | `GET /action/emailTemplates/list` | [docs](https://help.withmoxie.com/en/articles/8260211-list-email-templates) |
| [List Form Names](actions/list-form-names.md) | `GET /action/formNames/list` | [docs](https://help.withmoxie.com/en/articles/8260225-list-form-names) |
| [List Invoice Templates](actions/list-invoice-templates.md) | `GET /action/invoiceTemplates/list` | [docs](https://help.withmoxie.com/en/articles/8260216-list-invoice-templates) |
| [List Pipeline Stages](actions/list-pipeline-stages.md) | `GET /action/pipelineStages/list` | [docs](https://help.withmoxie.com/en/articles/8260232-list-pipeline-stages) |
| [List Project Task Stages](actions/list-project-task-stages.md) | `GET /action/taskStages/list` | [docs](https://help.withmoxie.com/en/articles/8260242-list-project-task-stages) |
| [List Vendor Names](actions/list-vendor-names.md) | `GET /action/vendors/list` | [docs](https://help.withmoxie.com/en/articles/8260220-list-vendor-names) |
| [List Workspace Users](actions/list-workspace-users.md) | `GET /action/users/list` | [docs](https://help.withmoxie.com/en/articles/8260260-list-workspace-users) |
| [Search Clients](actions/search-clients.md) | `GET /action/clients/search` | [docs](https://help.withmoxie.com/en/articles/8163928-search-clients) |
| [Search Contacts](actions/search-contacts.md) | `GET /action/contacts/search` | [docs](https://help.withmoxie.com/en/articles/8259974-search-contacts) |
| [Search Payable Invoices](actions/search-payable-invoices.md) | `GET /action/payableInvoices/search` | [docs](https://help.withmoxie.com/en/articles/8260252-search-payable-invoices) |
| [Search Projects](actions/search-projects.md) | `GET /action/projects/search` | [docs](https://help.withmoxie.com/en/articles/8260204-search-projects) |
