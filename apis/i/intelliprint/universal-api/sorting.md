# Intelliprint Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Intelliprint expects, and each action page lists the fields available to sort.

## Intelliprint actions that support sorting

- [List Backgrounds](actions/list-backgrounds.md)
- [List Mailing List Recipients](actions/list-mailing-list-recipients.md)
- [List Mailing Lists](actions/list-mailing-lists.md)
- [List Print Jobs](actions/list-print-jobs.md)
