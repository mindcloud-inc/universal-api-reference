# Simplecast Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Simplecast expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-podcast-episodes?connectionId=$CONNECTION_ID&limit=25&offset=0&podcastId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Simplecast actions that support pagination

- [List Podcast Episodes](actions/list-podcast-episodes.md)
- [List Podcasts](actions/list-podcasts.md)
- [List Season Episodes](actions/list-season-episodes.md)
