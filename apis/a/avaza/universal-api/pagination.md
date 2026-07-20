# Avaza Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Avaza expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-bill-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Avaza actions that support pagination

- [List Bill Payments](actions/list-bill-payments.md)
- [List Bills](actions/list-bills.md)
- [List Companies](actions/list-companies.md)
- [List Companies Lookup](actions/list-companies-lookup.md)
- [List Contacts](actions/list-contacts.md)
- [List Credit Notes](actions/list-credit-notes.md)
- [List Estimates](actions/list-estimates.md)
- [List Expense Groups Lookup](actions/list-expense-groups-lookup.md)
- [List Expense Merchants Lookup](actions/list-expense-merchants-lookup.md)
- [List Expenses](actions/list-expenses.md)
- [List Fixed Amounts](actions/list-fixed-amounts.md)
- [List Inventories](actions/list-inventories.md)
- [List Invoices](actions/list-invoices.md)
- [List Payments](actions/list-payments.md)
- [List Projects](actions/list-projects.md)
- [List Projects Lookup](actions/list-projects-lookup.md)
- [List Recurring Invoices](actions/list-recurring-invoices.md)
- [List Schedule Assignments](actions/list-schedule-assignments.md)
- [List Schedule Series](actions/list-schedule-series.md)
- [List Tasks](actions/list-tasks.md)
- [List Tasks Lookup](actions/list-tasks-lookup.md)
- [List Timesheets](actions/list-timesheets.md)
