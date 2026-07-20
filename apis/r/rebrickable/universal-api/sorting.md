# Rebrickable Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Rebrickable expects, and each action page lists the fields available to sort.

## Rebrickable actions that support sorting

- [List Alternate Builds for Set](actions/list-alternate-builds-for-set.md)
- [List Badges](actions/list-badges.md)
- [List Colors](actions/list-colors.md)
- [List Minifigs](actions/list-minifigs.md)
- [List Part Categories](actions/list-part-categories.md)
- [List Part Colors](actions/list-part-colors.md)
- [List Parts](actions/list-parts.md)
- [List Sets](actions/list-sets.md)
- [List Sets Containing Minifig](actions/list-sets-containing-minifig.md)
- [List Sets Containing Part Color](actions/list-sets-containing-part-color.md)
- [List Themes](actions/list-themes.md)
