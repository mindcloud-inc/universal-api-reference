# Merge Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Merge expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merge/latest/actions/list-accounting-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0&accountToken=linked-account-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Merge actions that support pagination

- [List Accounting Invoices](actions/list-accounting-invoices.md)
- [List Accounting Linked Accounts](actions/list-accounting-linked-accounts.md)
- [List Accounting Payments](actions/list-accounting-payments.md)
- [List ATS Candidates](actions/list-ats-candidates.md)
- [List ATS Jobs](actions/list-ats-jobs.md)
- [List ATS Linked Accounts](actions/list-ats-linked-accounts.md)
- [List CRM Accounts](actions/list-crm-accounts.md)
- [List CRM Contacts](actions/list-crm-contacts.md)
- [List CRM Linked Accounts](actions/list-crm-linked-accounts.md)
- [List HRIS Companies](actions/list-hris-companies.md)
- [List HRIS Employees](actions/list-hris-employees.md)
- [List HRIS Linked Accounts](actions/list-hris-linked-accounts.md)
- [List Ticketing Linked Accounts](actions/list-ticketing-linked-accounts.md)
- [List Ticketing Tickets](actions/list-ticketing-tickets.md)
- [List Ticketing Users](actions/list-ticketing-users.md)
