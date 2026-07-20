# Booqable Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Booqable expects, and each action page lists the fields available to sort.

## Booqable actions that support sorting

- [List Customers](actions/list-customers.md)
- [List Items](actions/list-items.md)
- [List Orders](actions/list-orders.md)
- [List Products](actions/list-products.md)
- [List Stock Items](actions/list-stock-items.md)
- [Search Customers](actions/search-customers.md)
- [Search Items](actions/search-items.md)
- [Search Orders](actions/search-orders.md)
- [Search Products](actions/search-products.md)
