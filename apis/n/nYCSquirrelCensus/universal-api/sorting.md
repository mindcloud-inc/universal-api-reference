# NYC Squirrel Census Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format NYC Squirrel Census expects, and each action page lists the fields available to sort.

## NYC Squirrel Census actions that support sorting

- [List squirrel sightings](actions/list-squirrel-sightings.md)
