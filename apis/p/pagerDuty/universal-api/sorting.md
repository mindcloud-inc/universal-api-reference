# PagerDuty Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format PagerDuty expects, and each action page lists the fields available to sort.

## PagerDuty actions that support sorting

- [List Escalation Policies](actions/list-escalation-policies.md)
- [List Incidents](actions/list-incidents.md)
- [List Services](actions/list-services.md)
