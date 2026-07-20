# Print.one Postcards Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Print.one Postcards expects, and each action page lists the fields available to sort.

## Print.one Postcards actions that support sorting

- [List Batch Orders](actions/list-batch-orders.md)
- [List Batches](actions/list-batches.md)
- [List Custom Files](actions/list-custom-files.md)
- [List Orders](actions/list-orders.md)
- [List Templates](actions/list-templates.md)
