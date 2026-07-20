# BlogIn Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format BlogIn expects, and each action page lists the fields available to sort.

## BlogIn actions that support sorting

- [List Categories](actions/list-categories.md)
- [List Members](actions/list-members.md)
- [List Pages](actions/list-pages.md)
- [List Posts](actions/list-posts.md)
- [List Tags](actions/list-tags.md)
- [List Teams](actions/list-teams.md)
