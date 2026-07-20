# Float Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Float expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Float actions that support pagination

- [List Clients](actions/list-clients.md)
- [List Milestones](actions/list-milestones.md)
- [List People](actions/list-people.md)
- [List Phases](actions/list-phases.md)
- [List Project Tasks](actions/list-project-tasks.md)
- [List Projects](actions/list-projects.md)
- [List Roles](actions/list-roles.md)
