# Mediastack Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Mediastack expects, and each action page lists the fields available to sort.

## Mediastack actions that support sorting

- [Search Historical News](actions/search-historical-news.md)
- [Search News](actions/search-news.md)
