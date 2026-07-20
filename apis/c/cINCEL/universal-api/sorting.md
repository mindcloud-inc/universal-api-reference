# CINCEL Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format CINCEL expects, and each action page lists the fields available to sort.

## CINCEL actions that support sorting

- [List Document Invites](actions/list-document-invites.md)
- [List Folders](actions/list-folders.md)
- [List Team Users](actions/list-team-users.md)
- [List User Documents](actions/list-user-documents.md)
- [List User Teams](actions/list-user-teams.md)
- [List Users](actions/list-users.md)
