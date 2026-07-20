# Mailcoach Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Mailcoach expects, and each action page lists the fields available to sort.

## Mailcoach actions that support sorting

- [List Email Lists](actions/list-email-lists.md)
- [List Subscribers](actions/list-subscribers.md)
- [List Templates](actions/list-templates.md)
