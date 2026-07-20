# Microsoft 365 Planner Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Microsoft 365 Planner expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Planner/latest/actions/list-group-plans?connectionId=$CONNECTION_ID&limit=25&offset=0&groupId=9b1f3c7a-1234-4abc-9def-123456789abc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Microsoft 365 Planner actions that support pagination

- [List Group Plans](actions/list-group-plans.md)
- [List Groups](actions/list-groups.md)
- [List My Plans](actions/list-my-plans.md)
- [List Plan Tasks](actions/list-plan-tasks.md)
