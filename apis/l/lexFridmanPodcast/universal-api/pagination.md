# Lex Fridman Podcast Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Lex Fridman Podcast expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/list-blocks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Lex Fridman Podcast actions that support pagination

- [List Blocks](actions/list-blocks.md)
- [List Categories](actions/list-categories.md)
- [List Comments](actions/list-comments.md)
- [List Media](actions/list-media.md)
- [List Navigation Menus](actions/list-navigation-menus.md)
- [List Pages](actions/list-pages.md)
- [List Pattern Categories](actions/list-pattern-categories.md)
- [List Posts](actions/list-posts.md)
- [List Posts By Author](actions/list-posts-by-author.md)
- [List Posts By Category](actions/list-posts-by-category.md)
- [List Tags](actions/list-tags.md)
- [List Users](actions/list-users.md)
- [Search Categories](actions/search-categories.md)
- [Search Content](actions/search-content.md)
- [Search Media](actions/search-media.md)
- [Search Pages](actions/search-pages.md)
- [Search Posts](actions/search-posts.md)
- [Search Tags](actions/search-tags.md)
- [Search Terms](actions/search-terms.md)
- [Search Users](actions/search-users.md)
