# XenForo Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format XenForo expects, and each action page lists the fields available to sort.

## XenForo actions that support sorting

- [Get Forum Threads](actions/get-forum-threads.md)
- [Get Thread](actions/get-thread.md)
- [Get Thread Posts](actions/get-thread-posts.md)
- [Get Threads](actions/get-threads.md)
