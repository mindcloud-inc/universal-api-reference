# Contentful Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Contentful expects, and each action page lists the fields available to sort.

## Contentful actions that support sorting

- [List assets](actions/list-assets.md)
- [List content types](actions/list-content-types.md)
- [List entries](actions/list-entries.md)
- [List environment aliases](actions/list-environment-aliases.md)
- [List environments](actions/list-environments.md)
- [List locales](actions/list-locales.md)
- [List spaces](actions/list-spaces.md)
