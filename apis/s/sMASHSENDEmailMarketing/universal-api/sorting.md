# SMASHSEND Email Marketing Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format SMASHSEND Email Marketing expects, and each action page lists the fields available to sort.

## SMASHSEND Email Marketing actions that support sorting

- [List Contact Properties](actions/list-contact-properties.md)
- [List Contacts](actions/list-contacts.md)
