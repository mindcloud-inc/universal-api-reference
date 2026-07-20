# actiTIME Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format actiTIME expects, and each action page lists the fields available to sort.

## actiTIME actions that support sorting

- [List Customers](actions/list-customers.md)
- [List Departments](actions/list-departments.md)
- [List Leave Types](actions/list-leave-types.md)
- [List Projects](actions/list-projects.md)
- [List Tasks](actions/list-tasks.md)
- [List Time Zone Groups](actions/list-time-zone-groups.md)
- [List Types of Work](actions/list-types-of-work.md)
- [List Users](actions/list-users.md)
- [List Workflow Statuses](actions/list-workflow-statuses.md)
