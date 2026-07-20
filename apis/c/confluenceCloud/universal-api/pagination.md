# Confluence Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Confluence expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-attachments-for-page?connectionId=$CONNECTION_ID&limit=25&offset=0&cloudId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Confluence actions that support pagination

- [List Attachments For Page](actions/list-attachments-for-page.md)
- [List Blog Posts](actions/list-blog-posts.md)
- [List Blog Posts In Space](actions/list-blog-posts-in-space.md)
- [List Footer Comments](actions/list-footer-comments.md)
- [List Footer Comments For Page](actions/list-footer-comments-for-page.md)
- [List Inline Comments For Page](actions/list-inline-comments-for-page.md)
- [List Labels For Page](actions/list-labels-for-page.md)
- [List Pages](actions/list-pages.md)
- [List Pages In Space](actions/list-pages-in-space.md)
- [List Spaces](actions/list-spaces.md)
- [List Tasks](actions/list-tasks.md)
