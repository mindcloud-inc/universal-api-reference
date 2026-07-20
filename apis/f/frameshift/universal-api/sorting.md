# Frameshift Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Frameshift expects, and each action page lists the fields available to sort.

## Frameshift actions that support sorting

- [List All Sample Files](actions/list-all-sample-files.md)
- [List Project Activities](actions/list-project-activities.md)
- [List Project Files](actions/list-project-files.md)
- [List Project Variants](actions/list-project-variants.md)
- [List Projects](actions/list-projects.md)
- [List Sample Files](actions/list-sample-files.md)
