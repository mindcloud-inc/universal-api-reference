# Fingertip Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Fingertip expects, and each action page lists the fields available to sort.

## Fingertip actions that support sorting

- [List Blog Posts](actions/list-blog-posts.md)
- [List Event Types](actions/list-event-types.md)
- [List Form Templates](actions/list-form-templates.md)
- [List Invoices](actions/list-invoices.md)
- [List Webhooks](actions/list-webhooks.md)
- [List Workspaces](actions/list-workspaces.md)
