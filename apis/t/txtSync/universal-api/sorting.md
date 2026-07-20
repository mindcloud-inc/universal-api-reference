# TxtSync Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format TxtSync expects, and each action page lists the fields available to sort.

## TxtSync actions that support sorting

- [List Contact Tags](actions/list-contact-tags.md)
- [List Contacts](actions/list-contacts.md)
- [List Tags](actions/list-tags.md)
