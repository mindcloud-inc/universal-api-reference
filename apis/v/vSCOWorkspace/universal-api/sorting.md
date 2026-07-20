# VSCO Workspace Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format VSCO Workspace expects, and each action page lists the fields available to sort.

## VSCO Workspace actions that support sorting

- [List Contacts](actions/list-contacts.md)
- [List Events](actions/list-events.md)
- [List Files](actions/list-files.md)
- [List Galleries](actions/list-galleries.md)
- [List Jobs](actions/list-jobs.md)
- [List Orders](actions/list-orders.md)
- [List Orders for Job](actions/list-orders-for-job.md)
- [List Payments](actions/list-payments.md)
- [List Payments for Job](actions/list-payments-for-job.md)
