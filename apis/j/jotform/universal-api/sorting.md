# Jotform Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Jotform expects, and each action page lists the fields available to sort.

## Jotform actions that support sorting

- [List Form Submissions](actions/list-form-submissions.md)
- [List Sub-User Accounts](actions/list-sub-user-accounts.md)
- [List User Forms](actions/list-user-forms.md)
- [List User History](actions/list-user-history.md)
- [List User Invoices](actions/list-user-invoices.md)
- [List User Reports](actions/list-user-reports.md)
- [List User Submissions](actions/list-user-submissions.md)
