# Incontrol Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Incontrol expects, and each action page lists the fields available to sort.

## Incontrol actions that support sorting

- [List Case Notes](actions/list-case-notes.md)
- [List Cases](actions/list-cases.md)
- [List Documents](actions/list-documents.md)
- [List Drafts](actions/list-drafts.md)
- [List Form Templates](actions/list-form-templates.md)
- [List Forms](actions/list-forms.md)
- [List Local Data Connectors](actions/list-local-data-connectors.md)
- [List Notifications](actions/list-notifications.md)
- [List Organizations](actions/list-organizations.md)
- [List Tasks](actions/list-tasks.md)
- [List Users](actions/list-users.md)
