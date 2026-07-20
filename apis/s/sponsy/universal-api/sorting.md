# Sponsy Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Sponsy expects, and each action page lists the fields available to sort.

## Sponsy actions that support sorting

- [List Publication Placements](actions/list-publication-placements.md)
- [List Publication Slots](actions/list-publication-slots.md)
- [List Publication Statuses](actions/list-publication-statuses.md)
- [List Publications](actions/list-publications.md)
