# CDC Content Services Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format CDC Content Services expects, and each action page lists the fields available to sort.

## CDC Content Services actions that support sorting

- [List Audiences](actions/list-audiences.md)
- [List Languages](actions/list-languages.md)
- [List Media](actions/list-media.md)
- [List Media By Tag](actions/list-media-by-tag.md)
- [List Media Types](actions/list-media-types.md)
- [List Organization Types](actions/list-organization-types.md)
- [List Organizations](actions/list-organizations.md)
- [List Sources](actions/list-sources.md)
- [List Tag Types](actions/list-tag-types.md)
- [List Tags](actions/list-tags.md)
- [List Topics](actions/list-topics.md)
