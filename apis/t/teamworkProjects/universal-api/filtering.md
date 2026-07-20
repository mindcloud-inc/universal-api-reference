# Teamwork Projects Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Teamwork Projects expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Teamwork Projects actions that support filtering

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
- [List Sample Projects](actions/list-sample-projects.md)
- [List Skills](actions/list-skills.md)
- [List Tags](actions/list-tags.md)
- [List Task Comments](actions/list-task-comments.md)
- [List Task Lists](actions/list-task-lists.md)
- [List Task Time Entries](actions/list-task-time-entries.md)
- [List Tasks](actions/list-tasks.md)
- [List Time Entries](actions/list-time-entries.md)
- [List Timesheets](actions/list-timesheets.md)
