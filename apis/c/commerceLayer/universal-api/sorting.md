# Commerce Layer Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Commerce Layer expects, and each action page lists the fields available to sort.

## Commerce Layer actions that support sorting

- [List Addresses](actions/list-addresses.md)
- [List Inventory Models](actions/list-inventory-models.md)
- [List Manual Tax Calculators](actions/list-manual-tax-calculators.md)
- [List Markets](actions/list-markets.md)
- [List Merchants](actions/list-merchants.md)
- [List Price Lists](actions/list-price-lists.md)
- [List Shipping Categories](actions/list-shipping-categories.md)
- [List Stock Locations](actions/list-stock-locations.md)
- [List Tax Categories](actions/list-tax-categories.md)
- [List Tax Rules](actions/list-tax-rules.md)
