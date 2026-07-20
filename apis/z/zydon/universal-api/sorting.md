# Zydon Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Zydon expects, and each action page lists the fields available to sort.

## Zydon actions that support sorting

- [List Brands](actions/list-brands.md)
- [List Categories](actions/list-categories.md)
- [List Companies](actions/list-companies.md)
- [List Financials](actions/list-financials.md)
- [List Measure Units](actions/list-measure-units.md)
- [List Orders](actions/list-orders.md)
- [List Partners](actions/list-partners.md)
- [List Payment Methods](actions/list-payment-methods.md)
- [List Price Tables](actions/list-price-tables.md)
- [List Products](actions/list-products.md)
- [List Profiles](actions/list-profiles.md)
- [List Sales](actions/list-sales.md)
- [List Sellers](actions/list-sellers.md)
- [List Variations](actions/list-variations.md)
- [List Warehouses](actions/list-warehouses.md)
