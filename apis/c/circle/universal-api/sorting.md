# Circle Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Circle expects, and each action page lists the fields available to sort.

## Circle actions that support sorting

- [List Basic Posts](actions/list-basic-posts.md)
- [List Events](actions/list-events.md)
- [List Member Tags](actions/list-member-tags.md)
- [List Spaces](actions/list-spaces.md)
- [List Topics](actions/list-topics.md)
