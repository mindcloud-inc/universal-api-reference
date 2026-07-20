# <img src="https://images.mindcloud.co/apps/icons/merge_1776093367233.png" alt="Merge logo" width="28" height="28"> Merge: Universal API

Use Merge Unified API endpoints for linked accounts plus HRIS, ATS, Accounting, Ticketing, and CRM data reads.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/merge/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.merge.dev
- **Vendor API docs:** https://docs.merge.dev/merge-unified/unified-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List HRIS Linked Accounts](actions/list-hris-linked-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merge/latest/actions/list-hris-linked-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Candidates

| Action | Method | Description |
| --- | --- | --- |
| [Get ATS Candidate](actions/get-ats-candidate.md) | GET |  |
| [List ATS Candidates](actions/list-ats-candidates.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get CRM Account](actions/get-crm-account.md) | GET |  |
| [Get HRIS Company](actions/get-hris-company.md) | GET |  |
| [List CRM Accounts](actions/list-crm-accounts.md) | GET |  |
| [List HRIS Companies](actions/list-hris-companies.md) | GET |  |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Get Accounting Linked Account](actions/get-accounting-linked-account.md) | GET |  |
| [Get ATS Linked Account](actions/get-ats-linked-account.md) | GET |  |
| [Get CRM Linked Account](actions/get-crm-linked-account.md) | GET |  |
| [Get HRIS Linked Account](actions/get-hris-linked-account.md) | GET |  |
| [Get Ticketing Linked Account](actions/get-ticketing-linked-account.md) | GET |  |
| [List Accounting Linked Accounts](actions/list-accounting-linked-accounts.md) | GET |  |
| [List ATS Linked Accounts](actions/list-ats-linked-accounts.md) | GET |  |
| [List CRM Linked Accounts](actions/list-crm-linked-accounts.md) | GET |  |
| [List HRIS Linked Accounts](actions/list-hris-linked-accounts.md) | GET |  |
| [List Ticketing Linked Accounts](actions/list-ticketing-linked-accounts.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get CRM Contact](actions/get-crm-contact.md) | GET |  |
| [List CRM Contacts](actions/list-crm-contacts.md) | GET |  |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get HRIS Employee](actions/get-hris-employee.md) | GET |  |
| [List HRIS Employees](actions/list-hris-employees.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Accounting Invoice](actions/get-accounting-invoice.md) | GET |  |
| [List Accounting Invoices](actions/list-accounting-invoices.md) | GET |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get ATS Job](actions/get-ats-job.md) | GET |  |
| [List ATS Jobs](actions/list-ats-jobs.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Get Accounting Payment](actions/get-accounting-payment.md) | GET |  |
| [List Accounting Payments](actions/list-accounting-payments.md) | GET |  |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticketing Ticket](actions/get-ticketing-ticket.md) | GET |  |
| [List Ticketing Tickets](actions/list-ticketing-tickets.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticketing User](actions/get-ticketing-user.md) | GET |  |
| [List Ticketing Users](actions/list-ticketing-users.md) | GET |  |

