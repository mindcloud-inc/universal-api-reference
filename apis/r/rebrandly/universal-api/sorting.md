# Rebrandly Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Rebrandly expects, and each action page lists the fields available to sort.

## Rebrandly actions that support sorting

- [List Domains](actions/list-domains.md)
- [List Links](actions/list-links.md)
- [List Scripts](actions/list-scripts.md)
- [List Tags](actions/list-tags.md)
