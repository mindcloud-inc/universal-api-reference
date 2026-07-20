# Swell Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Swell expects, and each action page lists the fields available to sort.

## Swell actions that support sorting

- [List Accounts](actions/list-accounts.md)
- [List Carts](actions/list-carts.md)
- [List Categories](actions/list-categories.md)
- [List Coupons](actions/list-coupons.md)
- [List Orders](actions/list-orders.md)
- [List Products](actions/list-products.md)
- [List Promotions](actions/list-promotions.md)
- [List Variants](actions/list-variants.md)
