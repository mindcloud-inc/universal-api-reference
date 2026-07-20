# Cakemail Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Cakemail expects, and each action page lists the fields available to sort.

## Cakemail actions that support sorting

- [List Campaigns](actions/list-campaigns.md)
- [List Contacts](actions/list-contacts.md)
- [List Lists](actions/list-lists.md)
- [List Senders](actions/list-senders.md)
