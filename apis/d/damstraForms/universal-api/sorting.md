# Damstra Forms Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Damstra Forms expects, and each action page lists the fields available to sort.

## Damstra Forms actions that support sorting

- [List Actions](actions/list-actions.md)
- [List Drawing Annotations](actions/list-drawing-annotations.md)
- [List Drawing Views](actions/list-drawing-views.md)
- [List Drawings](actions/list-drawings.md)
- [List Forms](actions/list-forms.md)
- [List Memos](actions/list-memos.md)
- [List Organisation Lists](actions/list-organisation-lists.md)
- [List Projects](actions/list-projects.md)
- [List Punch Lists](actions/list-punch-lists.md)
- [List Templates](actions/list-templates.md)
- [List Users](actions/list-users.md)
