# Brightpearl Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Brightpearl expects, and each action page lists the fields available to sort.

## Brightpearl actions that support sorting

- [List Goods-In Notes](actions/list-goods-in-notes.md)
- [List Goods-Out Notes](actions/list-goods-out-notes.md)
- [List Orders](actions/list-orders.md)
