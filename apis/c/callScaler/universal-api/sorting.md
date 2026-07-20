# CallScaler Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format CallScaler expects, and each action page lists the fields available to sort.

## CallScaler actions that support sorting

- [Export Calls CSV](actions/export-calls-csv.md)
- [Get Call Analytics](actions/get-call-analytics.md)
- [List Calls](actions/list-calls.md)
