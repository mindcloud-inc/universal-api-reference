# Previsto Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Previsto expects, and each action page lists the fields available to sort.

## Previsto actions that support sorting

- [List Assignments](actions/list-assignments.md)
- [List Contacts](actions/list-contacts.md)
- [List Organizations](actions/list-organizations.md)
- [List Service Agreements](actions/list-service-agreements.md)
