# Longreads Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Longreads expects, and each action page lists the fields available to sort.

## Longreads actions that support sorting

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
- [Search Tags](actions/search-tags.md)
