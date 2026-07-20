# Vimeo Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Vimeo expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-available-video-showcases?connectionId=$CONNECTION_ID&limit=25&offset=0&videoId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Vimeo actions that support pagination

- [List Available Video Showcases](actions/list-available-video-showcases.md)
- [List Channel Videos](actions/list-channel-videos.md)
- [List Channels](actions/list-channels.md)
- [List Comment Replies](actions/list-comment-replies.md)
- [List Project Videos](actions/list-project-videos.md)
- [List Projects](actions/list-projects.md)
- [List Showcase Videos](actions/list-showcase-videos.md)
- [List Showcases](actions/list-showcases.md)
- [List User Videos](actions/list-user-videos.md)
- [List Video Comments](actions/list-video-comments.md)
- [List Video Tags](actions/list-video-tags.md)
- [List Videos with Tag](actions/list-videos-with-tag.md)
- [Search Videos](actions/search-videos.md)
