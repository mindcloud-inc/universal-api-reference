# UiPath Orchestrator Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model UiPath Orchestrator expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uiPathOrchestrator/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## UiPath Orchestrator actions that support pagination

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
