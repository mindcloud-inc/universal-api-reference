# Smoove Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Smoove expects, and each action page lists the fields available to sort.

## Smoove actions that support sorting

- [List Active Contacts](actions/list-active-contacts.md)
- [List Contact Lists](actions/list-contact-lists.md)
- [List Contacts In List](actions/list-contacts-in-list.md)
- [List Unsubscribed Contacts](actions/list-unsubscribed-contacts.md)
