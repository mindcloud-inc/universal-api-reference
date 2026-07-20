# AITable.ai Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model AITable.ai expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-nodes?connectionId=$CONNECTION_ID&limit=25&offset=0&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## AITable.ai actions that support pagination

- [List Nodes](actions/list-nodes.md)
- [List Records](actions/list-records.md)
- [List Role Units](actions/list-role-units.md)
- [List Roles](actions/list-roles.md)
- [List Sub Teams](actions/list-sub-teams.md)
- [List Team Members](actions/list-team-members.md)
