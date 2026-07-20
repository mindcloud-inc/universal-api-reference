# SchoolDigger Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format SchoolDigger expects, and each action page lists the fields available to sort.

## SchoolDigger actions that support sorting

- [Search Districts](actions/search-districts.md)
- [Search Schools](actions/search-schools.md)
