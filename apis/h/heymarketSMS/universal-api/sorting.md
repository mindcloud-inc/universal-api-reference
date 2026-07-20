# Heymarket SMS Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Heymarket SMS expects, and each action page lists the fields available to sort.

## Heymarket SMS actions that support sorting

- [List Contacts](actions/list-contacts.md)
- [List Conversations](actions/list-conversations.md)
- [List Team Messages](actions/list-team-messages.md)
