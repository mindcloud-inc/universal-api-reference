# Resco Cloud Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Resco Cloud expects, and each action page lists the fields available to sort.

## Resco Cloud actions that support sorting

- [List OData Entity Records](actions/list-o-data-entity-records.md)
- [List Questionnaire Results](actions/list-questionnaire-results.md)
- [Select Records](actions/select-records.md)
