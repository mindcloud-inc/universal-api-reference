# Dukaan Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Dukaan expects, and each action page lists the fields available to sort.

## Dukaan actions that support sorting

- [List Orders](actions/list-orders.md)
- [List Products](actions/list-products.md)
- [List Products By Category](actions/list-products-by-category.md)
- [List Store Audience](actions/list-store-audience.md)
- [Search Orders](actions/search-orders.md)
- [Search Products](actions/search-products.md)
