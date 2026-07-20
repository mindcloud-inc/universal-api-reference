# Oneflow Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Oneflow expects, and each action page lists the fields available to sort.

## Oneflow actions that support sorting

- [List Contacts](actions/list-contacts.md)
- [List Contract Data Fields](actions/list-contract-data-fields.md)
- [List Contract Files](actions/list-contract-files.md)
- [List Contracts](actions/list-contracts.md)
- [List Parties](actions/list-parties.md)
- [List Template Types](actions/list-template-types.md)
- [List Templates](actions/list-templates.md)
- [List Users](actions/list-users.md)
- [List Workspaces](actions/list-workspaces.md)
