# Flotiq Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Flotiq expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/list-content-objects?connectionId=$CONNECTION_ID&limit=25&offset=0&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Flotiq actions that support pagination

- [List Content Objects](actions/list-content-objects.md)
- [List Content Types](actions/list-content-types.md)
- [List Media Objects](actions/list-media-objects.md)
- [List Media Versions](actions/list-media-versions.md)
- [Search Content](actions/search-content.md)
