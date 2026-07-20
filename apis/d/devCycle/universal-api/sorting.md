# DevCycle Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format DevCycle expects, and each action page lists the fields available to sort.

## DevCycle actions that support sorting

- [List Audiences](actions/list-audiences.md)
- [List Custom Properties](actions/list-custom-properties.md)
- [List Environments](actions/list-environments.md)
- [List Feature Audit Entries](actions/list-feature-audit-entries.md)
- [List Features](actions/list-features.md)
- [List Metrics](actions/list-metrics.md)
- [List Project Stale Features](actions/list-project-stale-features.md)
- [List Projects](actions/list-projects.md)
- [List Variables](actions/list-variables.md)
- [List Webhooks](actions/list-webhooks.md)
