# Bannerbear Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Bannerbear expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/list-collections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Bannerbear actions that support pagination

- [List Collections](actions/list-collections.md)
- [List Images](actions/list-images.md)
- [List Movies](actions/list-movies.md)
- [List Template Sets](actions/list-template-sets.md)
- [List Templates](actions/list-templates.md)
- [List Videos](actions/list-videos.md)
