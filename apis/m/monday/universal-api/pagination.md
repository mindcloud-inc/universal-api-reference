# Monday Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Monday expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monday/latest/actions/get-boards-with-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Monday actions that support pagination

- [Get Board Items](actions/get-board-items.md)
- [Get Board Items by Column Value](actions/get-board-items-by-column-value.md)
- [Get Board Items with Sub Items](actions/get-board-items-sub-items.md)
- [Get Boards With items](actions/get-boards-with-items.md)
- [Get Boards With items (GraphQL)](actions/get-boards-with-items-graph-ql.md)
