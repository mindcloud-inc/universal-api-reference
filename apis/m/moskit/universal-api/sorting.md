# Moskit Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Moskit expects, and each action page lists the fields available to sort.

## Moskit actions that support sorting

- [List Activities](actions/list-activities.md)
- [List Companies](actions/list-companies.md)
- [List Contacts](actions/list-contacts.md)
- [List Deals](actions/list-deals.md)
- [List Projects](actions/list-projects.md)
- [List Users](actions/list-users.md)
- [Search Activities](actions/search-activities.md)
- [Search Companies](actions/search-companies.md)
- [Search Contacts](actions/search-contacts.md)
- [Search Deals](actions/search-deals.md)
- [Search Projects](actions/search-projects.md)
