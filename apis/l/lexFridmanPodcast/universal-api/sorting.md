# Lex Fridman Podcast Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Lex Fridman Podcast expects, and each action page lists the fields available to sort.

## Lex Fridman Podcast actions that support sorting

- [List Categories](actions/list-categories.md)
- [List Comments](actions/list-comments.md)
- [List Media](actions/list-media.md)
- [List Pages](actions/list-pages.md)
- [List Posts](actions/list-posts.md)
- [List Posts By Author](actions/list-posts-by-author.md)
- [List Posts By Category](actions/list-posts-by-category.md)
- [List Tags](actions/list-tags.md)
- [List Users](actions/list-users.md)
- [Search Categories](actions/search-categories.md)
- [Search Media](actions/search-media.md)
- [Search Pages](actions/search-pages.md)
- [Search Posts](actions/search-posts.md)
- [Search Tags](actions/search-tags.md)
- [Search Users](actions/search-users.md)
