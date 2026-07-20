# The Guardian Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model The Guardian expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/get-next-items?connectionId=$CONNECTION_ID&limit=25&offset=0&itemPath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## The Guardian actions that support pagination

- [Get Next Items](actions/get-next-items.md)
- [List Tags](actions/list-tags.md)
- [Search Content](actions/search-content.md)
