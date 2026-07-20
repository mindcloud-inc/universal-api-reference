# CRM in Cloud Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format CRM in Cloud expects, and each action page lists the fields available to sort.

## CRM in Cloud actions that support sorting

- [Search activities](actions/search-activities.md)
- [Search appointments](actions/search-appointments.md)
- [Search companies](actions/search-companies.md)
- [Search contacts](actions/search-contacts.md)
- [Search leads](actions/search-leads.md)
- [Search lists](actions/search-lists.md)
- [Search opportunities](actions/search-opportunities.md)
- [Search storage items](actions/search-storage-items.md)
