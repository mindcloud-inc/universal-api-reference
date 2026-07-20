# Switchy.io Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Switchy.io expects, and each action page lists the fields available to sort.

## Switchy.io actions that support sorting

- [List Domains](actions/list-domains.md)
- [List Folders](actions/list-folders.md)
- [List Link Scripts](actions/list-link-scripts.md)
- [List Links](actions/list-links.md)
- [List Pixels](actions/list-pixels.md)
- [List Tokens](actions/list-tokens.md)
- [List UTM Templates](actions/list-utm-templates.md)
