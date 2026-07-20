# Teamgate Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Teamgate expects, and each action page lists the fields available to sort.

## Teamgate actions that support sorting

- [List Activities](actions/list-activities.md)
- [List Companies](actions/list-companies.md)
- [List Custom Fields](actions/list-custom-fields.md)
- [List Deals](actions/list-deals.md)
- [List Lead Statuses](actions/list-lead-statuses.md)
- [List Leads](actions/list-leads.md)
- [List People](actions/list-people.md)
- [List Pipelines](actions/list-pipelines.md)
- [List Sources](actions/list-sources.md)
- [List Users](actions/list-users.md)
- [Search Companies](actions/search-companies.md)
- [Search Deals](actions/search-deals.md)
- [Search Leads](actions/search-leads.md)
- [Search People](actions/search-people.md)
