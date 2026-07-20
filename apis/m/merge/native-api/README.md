# Merge: Native API Reference

A consolidated summary of Merge's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.merge.dev/merge-unified/unified-api
- **API base URL:** `https://api.merge.dev`

## Authentication

### API Key

Authenticate Merge API requests with your Merge API key. Unified actions also require an Account Token input for the linked account being queried.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.merge.dev/basics/authentication/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `results`.

## Pagination

Use `page_size` in the query string to set the page size (maximum 100). Use `cursor` in the query string as the pagination cursor.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Accounting Invoice](actions/get-accounting-invoice.md) | `GET /api/accounting/v1/invoices/{id}` | [docs](https://docs.merge.dev/accounting/invoices/) |
| [Get Accounting Linked Account](actions/get-accounting-linked-account.md) | `GET /api/accounting/v1/linked-accounts/{id}` | [docs](https://docs.merge.dev/basics/linked-accounts/) |
| [Get Accounting Payment](actions/get-accounting-payment.md) | `GET /api/accounting/v1/payments/{id}` | [docs](https://docs.merge.dev/accounting/payments/) |
| [Get ATS Candidate](actions/get-ats-candidate.md) | `GET /api/ats/v1/candidates/{id}` | [docs](https://docs.merge.dev/ats/candidates/) |
| [Get ATS Job](actions/get-ats-job.md) | `GET /api/ats/v1/jobs/{id}` | [docs](https://docs.merge.dev/ats/jobs/) |
| [Get ATS Linked Account](actions/get-ats-linked-account.md) | `GET /api/ats/v1/linked-accounts/{id}` | [docs](https://docs.merge.dev/basics/linked-accounts/) |
| [Get CRM Account](actions/get-crm-account.md) | `GET /api/crm/v1/accounts/{id}` | [docs](https://docs.merge.dev/crm/accounts/) |
| [Get CRM Contact](actions/get-crm-contact.md) | `GET /api/crm/v1/contacts/{id}` | [docs](https://docs.merge.dev/crm/contacts/) |
| [Get CRM Linked Account](actions/get-crm-linked-account.md) | `GET /api/crm/v1/linked-accounts/{id}` | [docs](https://docs.merge.dev/basics/linked-accounts/) |
| [Get HRIS Company](actions/get-hris-company.md) | `GET /api/hris/v1/companies/{id}` | [docs](https://docs.merge.dev/hris/companies/) |
| [Get HRIS Employee](actions/get-hris-employee.md) | `GET /api/hris/v1/employees/{id}` | [docs](https://docs.merge.dev/hris/employees/) |
| [Get HRIS Linked Account](actions/get-hris-linked-account.md) | `GET /api/hris/v1/linked-accounts/{id}` | [docs](https://docs.merge.dev/basics/linked-accounts/) |
| [Get Ticketing Linked Account](actions/get-ticketing-linked-account.md) | `GET /api/ticketing/v1/linked-accounts/{id}` | [docs](https://docs.merge.dev/basics/linked-accounts/) |
| [Get Ticketing Ticket](actions/get-ticketing-ticket.md) | `GET /api/ticketing/v1/tickets/{id}` | [docs](https://docs.merge.dev/ticketing/tickets/) |
| [Get Ticketing User](actions/get-ticketing-user.md) | `GET /api/ticketing/v1/users/{id}` | [docs](https://docs.merge.dev/ticketing/users/) |
| [List Accounting Invoices](actions/list-accounting-invoices.md) | `GET /api/accounting/v1/invoices` | [docs](https://docs.merge.dev/accounting/invoices/) |
| [List Accounting Linked Accounts](actions/list-accounting-linked-accounts.md) | `GET /api/accounting/v1/linked-accounts` | [docs](https://docs.merge.dev/basics/linked-accounts/) |
| [List Accounting Payments](actions/list-accounting-payments.md) | `GET /api/accounting/v1/payments` | [docs](https://docs.merge.dev/accounting/payments/) |
| [List ATS Candidates](actions/list-ats-candidates.md) | `GET /api/ats/v1/candidates` | [docs](https://docs.merge.dev/ats/candidates/) |
| [List ATS Jobs](actions/list-ats-jobs.md) | `GET /api/ats/v1/jobs` | [docs](https://docs.merge.dev/ats/jobs/) |
| [List ATS Linked Accounts](actions/list-ats-linked-accounts.md) | `GET /api/ats/v1/linked-accounts` | [docs](https://docs.merge.dev/basics/linked-accounts/) |
| [List CRM Accounts](actions/list-crm-accounts.md) | `GET /api/crm/v1/accounts` | [docs](https://docs.merge.dev/crm/accounts/) |
| [List CRM Contacts](actions/list-crm-contacts.md) | `GET /api/crm/v1/contacts` | [docs](https://docs.merge.dev/crm/contacts/) |
| [List CRM Linked Accounts](actions/list-crm-linked-accounts.md) | `GET /api/crm/v1/linked-accounts` | [docs](https://docs.merge.dev/basics/linked-accounts/) |
| [List HRIS Companies](actions/list-hris-companies.md) | `GET /api/hris/v1/companies` | [docs](https://docs.merge.dev/hris/companies/) |
| [List HRIS Employees](actions/list-hris-employees.md) | `GET /api/hris/v1/employees` | [docs](https://docs.merge.dev/hris/employees/) |
| [List HRIS Linked Accounts](actions/list-hris-linked-accounts.md) | `GET /api/hris/v1/linked-accounts` | [docs](https://docs.merge.dev/basics/linked-accounts/) |
| [List Ticketing Linked Accounts](actions/list-ticketing-linked-accounts.md) | `GET /api/ticketing/v1/linked-accounts` | [docs](https://docs.merge.dev/basics/linked-accounts/) |
| [List Ticketing Tickets](actions/list-ticketing-tickets.md) | `GET /api/ticketing/v1/tickets` | [docs](https://docs.merge.dev/ticketing/tickets/) |
| [List Ticketing Users](actions/list-ticketing-users.md) | `GET /api/ticketing/v1/users` | [docs](https://docs.merge.dev/ticketing/users/) |
