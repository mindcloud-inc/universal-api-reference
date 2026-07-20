# Roger Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Roger expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roger/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Roger actions that support pagination

- [List Organizations](actions/list-organizations.md)
- [List People](actions/list-people.md)
- [List Segments](actions/list-segments.md)
- [List Tags](actions/list-tags.md)
- [List Tasks](actions/list-tasks.md)
- [List Webhooks](actions/list-webhooks.md)
- [List Workspaces](actions/list-workspaces.md)
