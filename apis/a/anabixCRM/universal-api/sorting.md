# Anabix CRM Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Anabix CRM expects, and each action page lists the fields available to sort.

## Anabix CRM actions that support sorting

- [List Activities](actions/list-activities.md)
- [List Contacts](actions/list-contacts.md)
- [List Deals](actions/list-deals.md)
- [List Lists](actions/list-lists.md)
- [List Organizations](actions/list-organizations.md)
- [List Tasks](actions/list-tasks.md)
