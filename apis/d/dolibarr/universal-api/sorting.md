# Dolibarr Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Dolibarr expects, and each action page lists the fields available to sort.

## Dolibarr actions that support sorting

- [List Agenda Events](actions/list-agenda-events.md)
- [List Categories](actions/list-categories.md)
- [List Documents](actions/list-documents.md)
- [List Email Templates](actions/list-email-templates.md)
- [List Users](actions/list-users.md)
