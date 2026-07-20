# ShopWired Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format ShopWired expects, and each action page lists the fields available to sort.

## ShopWired actions that support sorting

- [List active brands](actions/list-brands.md)
- [List categories](actions/list-categories.md)
- [List customers](actions/list-customers.md)
- [List filter groups](actions/list-filter-groups.md)
- [List incomplete orders](actions/list-incomplete-orders.md)
- [List newsletter subscribers](actions/list-newsletter-subscribers.md)
- [List orders](actions/list-orders.md)
- [List product reviews](actions/list-product-reviews.md)
- [List products](actions/list-products.md)
- [Search for orders](actions/search-orders.md)
- [Search products](actions/search-products.md)
