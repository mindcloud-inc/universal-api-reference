# Testlify Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Testlify expects, and each action page lists the fields available to sort.

## Testlify actions that support sorting

- [List Assessment Candidates](actions/list-assessment-candidates.md)
- [List Assessments](actions/list-assessments.md)
- [List Candidates](actions/list-candidates.md)
- [List Workspace Users](actions/list-workspace-users.md)
