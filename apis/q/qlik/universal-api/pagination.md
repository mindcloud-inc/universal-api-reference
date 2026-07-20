# Qlik Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Qlik expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/filter-groups?connectionId=$CONNECTION_ID&limit=25&offset=0&filter=name%20eq%20%22Analytics%20Team%22" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Qlik actions that support pagination

- [Filter Groups](actions/filter-groups.md)
- [Filter Users](actions/filter-users.md)
- [List Collection Items](actions/list-collection-items.md)
- [List Collections](actions/list-collections.md)
- [List Groups](actions/list-groups.md)
- [List Item Collections](actions/list-item-collections.md)
- [List Items](actions/list-items.md)
- [List Published Items](actions/list-published-items.md)
- [List Reload Tasks](actions/list-reload-tasks.md)
- [List Reloads](actions/list-reloads.md)
- [List Space Assignments](actions/list-space-assignments.md)
- [List Spaces](actions/list-spaces.md)
- [List Users](actions/list-users.md)
