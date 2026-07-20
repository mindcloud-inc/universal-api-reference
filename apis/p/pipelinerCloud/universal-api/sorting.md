# Pipeliner Cloud Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Pipeliner Cloud expects, and each action page lists the fields available to sort.

## Pipeliner Cloud actions that support sorting

- [List Accounts](actions/list-accounts.md)
- [List Activities](actions/list-activities.md)
- [List Contacts](actions/list-contacts.md)
- [List Leads](actions/list-leads.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Products](actions/list-products.md)
