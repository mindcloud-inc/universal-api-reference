# Microsoft Dynamics 365 Sales Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Microsoft Dynamics 365 Sales expects, and each action page lists the fields available to sort.

## Microsoft Dynamics 365 Sales actions that support sorting

- [List Accounts](actions/list-accounts.md)
- [List Contacts](actions/list-contacts.md)
- [List Custom Records](actions/list-custom-records.md)
- [List Leads](actions/list-leads.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Users](actions/list-users.md)
