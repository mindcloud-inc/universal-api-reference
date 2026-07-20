# Mediastack Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Mediastack expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mediastack/latest/actions/search-historical-news?connectionId=$CONNECTION_ID&limit=25&offset=0&date=2026-04-30%20or%202026-04-01%2C2026-04-30" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Mediastack actions that support pagination

- [Search Historical News](actions/search-historical-news.md)
- [Search News](actions/search-news.md)
- [Search News Sources](actions/search-news-sources.md)
