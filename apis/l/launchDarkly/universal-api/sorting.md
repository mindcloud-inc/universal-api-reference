# LaunchDarkly Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format LaunchDarkly expects, and each action page lists the fields available to sort.

## LaunchDarkly actions that support sorting

- [Evaluate Flags](actions/evaluate-flags.md)
- [List Environments](actions/list-environments.md)
- [List Feature Flags](actions/list-feature-flags.md)
- [List Members](actions/list-members.md)
- [List Projects](actions/list-projects.md)
- [List Segments](actions/list-segments.md)
- [Search Contexts](actions/search-contexts.md)
