# Pexels Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Pexels expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pexels/latest/actions/list-collection-media?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Pexels actions that support pagination

- [List Collection Media](actions/list-collection-media.md)
- [List Curated Photos](actions/list-curated-photos.md)
- [List Featured Collections](actions/list-featured-collections.md)
- [List My Collections](actions/list-my-collections.md)
- [List Popular Videos](actions/list-popular-videos.md)
- [Search Photos](actions/search-photos.md)
- [Search Videos](actions/search-videos.md)
