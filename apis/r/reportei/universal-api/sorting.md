# Reportei Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Reportei expects, and each action page lists the fields available to sort.

## Reportei actions that support sorting

- [List Dashboards](actions/list-dashboards.md)
- [List Integrations](actions/list-integrations.md)
- [List Projects](actions/list-projects.md)
- [List Reports](actions/list-reports.md)
- [List Timeline Events](actions/list-timeline-events.md)
- [List Webhooks](actions/list-webhooks.md)
