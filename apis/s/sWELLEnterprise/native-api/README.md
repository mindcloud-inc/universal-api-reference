# SWELLEnterprise: Native API Reference

A consolidated summary of SWELLEnterprise's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://dashboard.swellsystem.com/docs
- **API base URL:** `https://dashboard.swellsystem.com/api/v1`

## Authentication

### API Key

Authenticate SWELLEnterprise requests with a bearer API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dashboard.swellsystem.com/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 15; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Use `ascending` for ascending order and `-` for descending order. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve Project Approval](actions/approve-project-approval.md) | `POST /projects/projects/:project_id/approvals/:approval_id/approve` | [docs](https://dashboard.swellsystem.com/docs#endpoints-POSTapi-v1-projects-projects--project_id--approvals--approval_id--approve) |
| [Bulk Create Contacts](actions/bulk-create-contacts.md) | `POST /crm/contacts/bulk` | [docs](https://dashboard.swellsystem.com/docs#crm-contacts-POSTapi-v1-crm-contacts-bulk) |
| [Create Company](actions/create-company.md) | `POST /crm/companies` | [docs](https://dashboard.swellsystem.com/docs#crm-companies-POSTapi-v1-crm-companies) |
| [Create Contact](actions/create-contact.md) | `POST /crm/contacts` | [docs](https://dashboard.swellsystem.com/docs#crm-contacts-POSTapi-v1-crm-contacts) |
| [Create Estimate](actions/create-estimate.md) | `POST /finance/estimates` | [docs](https://dashboard.swellsystem.com/docs#finance-estimates-POSTapi-v1-finance-estimates) |
| [Create Invoice](actions/create-invoice.md) | `POST /finance/invoices` | [docs](https://dashboard.swellsystem.com/docs#finance-invoices-POSTapi-v1-finance-invoices) |
| [Create Lead](actions/create-lead.md) | `POST /crm/leads` | [docs](https://dashboard.swellsystem.com/docs#crm-leads-POSTapi-v1-crm-leads) |
| [Create Product](actions/create-product.md) | `POST /products/products` | [docs](https://dashboard.swellsystem.com/docs#products-POSTapi-v1-products-products) |
| [Create Project](actions/create-project.md) | `POST /projects/projects` | [docs](https://dashboard.swellsystem.com/docs#projects-POSTapi-v1-projects-projects) |
| [Create Project Approval](actions/create-project-approval.md) | `POST /projects/projects/:project_id/approvals` | [docs](https://dashboard.swellsystem.com/docs#endpoints-POSTapi-v1-projects-projects--project_id--approvals) |
| [Create Revision Request](actions/create-revision-request.md) | `POST /projects/projects/:project_id/revision-requests` | [docs](https://dashboard.swellsystem.com/docs#endpoints-POSTapi-v1-projects-projects--project_id--revision-requests) |
| [Create Task](actions/create-task.md) | `POST /projects/tasks` | [docs](https://dashboard.swellsystem.com/docs#projects-tasks-POSTapi-v1-projects-tasks) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /webhooks/subscriptions` | [docs](https://dashboard.swellsystem.com/docs#webhooks-POSTapi-v1-webhooks-subscriptions) |
| [Get Portal Configuration](actions/get-portal-configuration.md) | `GET /client-portal/config` | [docs](https://dashboard.swellsystem.com/docs#client-portal-GETapi-v1-client-portal-config) |
| [Get Portal Token](actions/get-portal-token.md) | `POST /client-portal/token` | [docs](https://dashboard.swellsystem.com/docs#client-portal-POSTapi-v1-client-portal-token) |
| [Invite Company To Portal](actions/invite-company-to-portal.md) | `POST /client-portal/companies/:companyId/invite` | [docs](https://dashboard.swellsystem.com/docs#client-portal-POSTapi-v1-client-portal-companies--companyId--invite) |
| [Invite Contact To Portal](actions/invite-contact-to-portal.md) | `POST /client-portal/contacts/:contactId/invite` | [docs](https://dashboard.swellsystem.com/docs#client-portal-POSTapi-v1-client-portal-contacts--contactId--invite) |
| [Regenerate Webhook Secret](actions/regenerate-webhook-secret.md) | `POST /webhooks/subscriptions/:id/regenerate-secret` | [docs](https://dashboard.swellsystem.com/docs#webhooks-POSTapi-v1-webhooks-subscriptions--id--regenerate-secret) |
| [Reject Project Approval](actions/reject-project-approval.md) | `POST /projects/projects/:project_id/approvals/:approval_id/reject` | [docs](https://dashboard.swellsystem.com/docs#endpoints-POSTapi-v1-projects-projects--project_id--approvals--approval_id--reject) |
| [Request Changes On Project Approval](actions/request-changes-on-project-approval.md) | `POST /projects/projects/:project_id/approvals/:approval_id/request-changes` | [docs](https://dashboard.swellsystem.com/docs#endpoints-POSTapi-v1-projects-projects--project_id--approvals--approval_id--request-changes) |
| [Update Webhook Subscription](actions/update-webhook-subscription.md) | `PUT /webhooks/subscriptions/:id` | [docs](https://dashboard.swellsystem.com/docs#webhooks-PUTapi-v1-webhooks-subscriptions--id-) |
