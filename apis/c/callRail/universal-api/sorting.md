# CallRail Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format CallRail expects, and each action page lists the fields available to sort.

## CallRail actions that support sorting

- [List Accounts](actions/list-accounts.md)
- [List Calls](actions/list-calls.md)
- [List Companies](actions/list-companies.md)
- [List Form Submissions](actions/list-form-submissions.md)
