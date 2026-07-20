# Teamwork Projects Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Teamwork Projects expects, and each action page lists the fields available to sort.

## Teamwork Projects actions that support sorting

- [List Comments](actions/list-comments.md)
- [List Companies](actions/list-companies.md)
- [List Messages](actions/list-messages.md)
- [List Milestones](actions/list-milestones.md)
- [List Notebooks](actions/list-notebooks.md)
- [List People](actions/list-people.md)
- [List Project Risks](actions/list-project-risks.md)
- [List Project Tasks](actions/list-project-tasks.md)
- [List Project Updates](actions/list-project-updates.md)
- [List Projects](actions/list-projects.md)
- [List Tags](actions/list-tags.md)
- [List Task Lists](actions/list-task-lists.md)
- [List Task Time Entries](actions/list-task-time-entries.md)
- [List Tasks](actions/list-tasks.md)
- [List Time Entries](actions/list-time-entries.md)
- [List Timesheets](actions/list-timesheets.md)
