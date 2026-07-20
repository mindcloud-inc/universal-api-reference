# Twitch Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Twitch expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-channel-followers?connectionId=$CONNECTION_ID&limit=25&offset=0&broadcasterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Twitch actions that support pagination

- [List Channel Followers](actions/list-channel-followers.md)
- [List Chatters](actions/list-chatters.md)
- [List Followed Streams](actions/list-followed-streams.md)
