# UiPath Orchestrator Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format UiPath Orchestrator expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## UiPath Orchestrator actions that support filtering

- [List assets](actions/list-assets.md)
- [List folders](actions/list-folders.md)
- [List jobs](actions/list-jobs.md)
- [List machines](actions/list-machines.md)
- [List processes](actions/list-processes.md)
- [List queue items](actions/list-queue-items.md)
- [List queues](actions/list-queues.md)
- [List robots](actions/list-robots.md)
- [List runtime licenses](actions/list-runtime-licenses.md)
- [List schedules](actions/list-schedules.md)
- [List settings](actions/list-settings.md)
- [List tasks across folders](actions/list-tasks-across-folders.md)
- [List tenants](actions/list-tenants.md)
- [List users](actions/list-users.md)
