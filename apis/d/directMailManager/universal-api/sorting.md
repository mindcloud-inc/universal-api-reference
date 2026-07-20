# Direct Mail Manager Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Direct Mail Manager expects, and each action page lists the fields available to sort.

## Direct Mail Manager actions that support sorting

- [List Addresses](actions/list-addresses.md)
- [List Custom Fields](actions/list-custom-fields.md)
- [List Letters](actions/list-letters.md)
- [List Mailing Lists](actions/list-mailing-lists.md)
- [List Postcards](actions/list-postcards.md)
- [List Segments](actions/list-segments.md)
