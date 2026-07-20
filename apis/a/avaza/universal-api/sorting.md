# Avaza Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Avaza expects, and each action page lists the fields available to sort.

## Avaza actions that support sorting

- [List Bills](actions/list-bills.md)
- [List Companies](actions/list-companies.md)
- [List Contacts](actions/list-contacts.md)
- [List Deleted Timesheets](actions/list-deleted-timesheets.md)
- [List Estimates](actions/list-estimates.md)
- [List Expenses](actions/list-expenses.md)
- [List Fixed Amounts](actions/list-fixed-amounts.md)
- [List Invoices](actions/list-invoices.md)
- [List Projects](actions/list-projects.md)
- [List Recurring Invoices](actions/list-recurring-invoices.md)
- [List Schedule Assignments](actions/list-schedule-assignments.md)
- [List Schedule Series](actions/list-schedule-series.md)
- [List Tasks](actions/list-tasks.md)
- [List Timesheets](actions/list-timesheets.md)
