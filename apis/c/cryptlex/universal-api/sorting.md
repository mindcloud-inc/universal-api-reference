# Cryptlex Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Cryptlex expects, and each action page lists the fields available to sort.

## Cryptlex actions that support sorting

- [List Activations](actions/list-activations.md)
- [List Licenses](actions/list-licenses.md)
- [List Products](actions/list-products.md)
- [List Releases](actions/list-releases.md)
- [List Users](actions/list-users.md)
- [List Webhooks](actions/list-webhooks.md)
