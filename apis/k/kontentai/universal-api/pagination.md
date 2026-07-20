# Kontent.ai Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Kontent.ai expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/list-content-items?connectionId=$CONNECTION_ID&limit=25&offset=0&environmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Kontent.ai actions that support pagination

- [List content items](actions/list-content-items.md)
- [List content types](actions/list-content-types.md)
- [List languages](actions/list-languages.md)
- [List taxonomy groups](actions/list-taxonomy-groups.md)
