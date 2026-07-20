# WooCommerce Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format WooCommerce expects, and each action page lists the fields available to sort.

## WooCommerce actions that support sorting

- [List Coupons](actions/list-coupons.md)
- [List Customers](actions/list-customers.md)
- [List Orders](actions/list-orders.md)
- [List Product Categories](actions/list-product-categories.md)
- [List Products](actions/list-products.md)
