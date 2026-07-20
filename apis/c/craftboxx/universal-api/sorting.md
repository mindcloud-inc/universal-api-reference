# Craftboxx Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Craftboxx expects, and each action page lists the fields available to sort.

## Craftboxx actions that support sorting

- [List Articles](actions/list-articles.md)
- [List Assignments](actions/list-assignments.md)
- [List Customers](actions/list-customers.md)
- [List Employees](actions/list-employees.md)
- [List Projects](actions/list-projects.md)
- [List Timesheets](actions/list-timesheets.md)
