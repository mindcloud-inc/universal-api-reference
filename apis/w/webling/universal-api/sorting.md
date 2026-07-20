# Webling Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Webling expects, and each action page lists the fields available to sort.

## Webling actions that support sorting

- [List Articles](actions/list-articles.md)
- [List Debitors](actions/list-debitors.md)
- [List Documentgroups](actions/list-documentgroups.md)
- [List Documents](actions/list-documents.md)
- [List Entries](actions/list-entries.md)
- [List Entrygroups](actions/list-entrygroups.md)
- [List Membergroups](actions/list-membergroups.md)
- [List Members](actions/list-members.md)
- [List Users](actions/list-users.md)
