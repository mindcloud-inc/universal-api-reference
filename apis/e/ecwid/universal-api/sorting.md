# Ecwid Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Ecwid expects, and each action page lists the fields available to sort.

## Ecwid actions that support sorting

- [Search Abandoned Carts](actions/search-abandoned-carts.md)
- [Search Customers](actions/search-customers.md)
- [Search Discount Coupons](actions/search-discount-coupons.md)
- [Search Orders](actions/search-orders.md)
- [Search Product Brands](actions/search-product-brands.md)
- [Search Products](actions/search-products.md)
