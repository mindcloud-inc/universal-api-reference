# GoSquared Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format GoSquared expects, and each action page lists the fields available to sort.

## GoSquared actions that support sorting

- [Get Person Feed](actions/get-person-feed.md)
- [List Smart Group People](actions/list-smart-group-people.md)
- [Search People](actions/search-people.md)
