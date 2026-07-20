# Keap Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Keap expects, and each action page lists the fields available to sort.

## Keap actions that support sorting

- [List Companies](actions/list-companies.md)
- [List Contacts](actions/list-contacts.md)
- [List Emails](actions/list-emails.md)
- [List Files](actions/list-files.md)
- [List Notes](actions/list-notes.md)
- [List Opportunities](actions/list-opportunities.md)
- [List Tags](actions/list-tags.md)
- [List Tasks](actions/list-tasks.md)
