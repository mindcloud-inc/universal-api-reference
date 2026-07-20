# Tumblr Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Tumblr expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-published-blog-posts?connectionId=$CONNECTION_ID&limit=25&offset=0&blogIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Tumblr actions that support pagination

- [Get Published Blog Posts](actions/get-published-blog-posts.md)
- [Get User Dashboard](actions/get-user-dashboard.md)
- [List Blog Blocks](actions/list-blog-blocks.md)
- [List Blog Followers](actions/list-blog-followers.md)
- [List Blog Following](actions/list-blog-following.md)
- [List Blog Likes](actions/list-blog-likes.md)
- [List Queued Posts](actions/list-queued-posts.md)
- [List User Following](actions/list-user-following.md)
- [List User Likes](actions/list-user-likes.md)
