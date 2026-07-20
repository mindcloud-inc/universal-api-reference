# Robopost Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Robopost expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/robopost/latest/actions/list-aggregated-analytics?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Robopost actions that support pagination

- [List Aggregated Analytics](actions/list-aggregated-analytics.md)
- [List GMB Threads for One Channel](actions/list-gmb-threads-for-one-channel.md)
- [List Social Inbox Items](actions/list-social-inbox-items.md)
- [List Social Inbox Threads Grouped by Post](actions/list-social-inbox-threads-grouped-by-post.md)
- [List Video Tasks](actions/list-video-tasks.md)
