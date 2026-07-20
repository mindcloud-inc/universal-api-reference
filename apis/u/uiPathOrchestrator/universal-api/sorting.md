# UiPath Orchestrator Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format UiPath Orchestrator expects, and each action page lists the fields available to sort.

## UiPath Orchestrator actions that support sorting

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
