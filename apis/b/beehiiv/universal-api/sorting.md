# Beehiiv Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Beehiiv expects, and each action page lists the fields available to sort.

## Beehiiv actions that support sorting

- [List Publication Email Blasts](actions/list-publication-email-blasts.md)
- [List Publication Engagements](actions/list-publication-engagements.md)
- [List Publication Posts](actions/list-publication-posts.md)
- [List Publications](actions/list-publications.md)
- [List Subscriptions](actions/list-subscriptions.md)
