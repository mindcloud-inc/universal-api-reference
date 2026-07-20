# Longreads Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Longreads expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Longreads actions that support pagination

- [List Categories](actions/list-categories.md)
- [List Categories By Slug](actions/list-categories-by-slug.md)
- [List Comments](actions/list-comments.md)
- [List Comments For Post](actions/list-comments-for-post.md)
- [List Guest Authors](actions/list-guest-authors.md)
- [List Media](actions/list-media.md)
- [List Pages](actions/list-pages.md)
- [List Pages By Slug](actions/list-pages-by-slug.md)
- [List Posts](actions/list-posts.md)
- [List Posts By Category](actions/list-posts-by-category.md)
- [List Posts By Slug](actions/list-posts-by-slug.md)
- [List Posts By Tag](actions/list-posts-by-tag.md)
- [List Posts Published After Date](actions/list-posts-published-after-date.md)
- [List Posts Published Before Date](actions/list-posts-published-before-date.md)
- [List Tags](actions/list-tags.md)
- [List Tags By Slug](actions/list-tags-by-slug.md)
- [Search Categories](actions/search-categories.md)
- [Search Comments](actions/search-comments.md)
- [Search Guest Authors](actions/search-guest-authors.md)
- [Search Media](actions/search-media.md)
- [Search Pages](actions/search-pages.md)
- [Search Posts](actions/search-posts.md)
- [Search Site Content](actions/search-site-content.md)
- [Search Tags](actions/search-tags.md)
