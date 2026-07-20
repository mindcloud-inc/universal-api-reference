# YouTube Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model YouTube expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0&part=snippet%2CcontentDetails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## YouTube actions that support pagination

- [List Activities](actions/list-activities.md)
- [List Channels](actions/list-channels.md)
- [List Comment Threads](actions/list-comment-threads.md)
- [List Comments](actions/list-comments.md)
- [List Playlist Items](actions/list-playlist-items.md)
- [List Playlists](actions/list-playlists.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Videos](actions/list-videos.md)
- [Search Videos](actions/search-videos.md)
