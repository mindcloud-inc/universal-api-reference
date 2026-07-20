# Emporix Commerce Engine Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Emporix Commerce Engine expects, and each action page lists the fields available to sort.

## Emporix Commerce Engine actions that support sorting

- [List Brands](actions/list-brands.md)
- [List Carts](actions/list-carts.md)
- [List Catalogs](actions/list-catalogs.md)
- [List Categories](actions/list-categories.md)
- [List Category Trees](actions/list-category-trees.md)
- [List Labels](actions/list-labels.md)
- [List Legal Entities](actions/list-legal-entities.md)
- [List Price Lists](actions/list-price-lists.md)
- [List Prices](actions/list-prices.md)
- [List Product Templates](actions/list-product-templates.md)
- [List Products](actions/list-products.md)
- [List Sales Orders](actions/list-sales-orders.md)
