# Systeme.io Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Systeme.io expects, and each action page lists the fields available to sort.

## Systeme.io actions that support sorting

- [List Community Memberships](actions/list-community-memberships.md)
- [List Contacts](actions/list-contacts.md)
- [List Tags](actions/list-tags.md)
