# HelpCrunch Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format HelpCrunch expects, and each action page lists the fields available to sort.

## HelpCrunch actions that support sorting

- [List Chats](actions/list-chats.md)
- [List Customers](actions/list-customers.md)
- [Search Chats](actions/search-chats.md)
- [Search Customers](actions/search-customers.md)
