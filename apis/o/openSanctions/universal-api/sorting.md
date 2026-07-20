# OpenSanctions Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format OpenSanctions expects, and each action page lists the fields available to sort.

## OpenSanctions actions that support sorting

- [List Adjacent Entities](actions/list-adjacent-entities.md)
- [List Adjacent Entities By Property](actions/list-adjacent-entities-by-property.md)
- [List Entity Statements](actions/list-entity-statements.md)
- [Search Entities](actions/search-entities.md)
