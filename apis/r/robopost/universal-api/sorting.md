# Robopost Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Robopost expects, and each action page lists the fields available to sort.

## Robopost actions that support sorting

- [List GMB Threads for One Channel](actions/list-gmb-threads-for-one-channel.md)
- [List Social Inbox Items](actions/list-social-inbox-items.md)
- [List Social Inbox Threads Grouped by Post](actions/list-social-inbox-threads-grouped-by-post.md)
- [List Video Tasks](actions/list-video-tasks.md)
