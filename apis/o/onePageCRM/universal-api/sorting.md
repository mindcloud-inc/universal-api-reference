# OnePageCRM Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format OnePageCRM expects, and each action page lists the fields available to sort.

## OnePageCRM actions that support sorting

- [List Action Stream Contacts](actions/list-action-stream-contacts.md)
- [List Actions](actions/list-actions.md)
- [List Companies](actions/list-companies.md)
- [List Contacts](actions/list-contacts.md)
- [List Deals](actions/list-deals.md)
- [List Notes](actions/list-notes.md)
