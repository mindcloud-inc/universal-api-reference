# inFlow Inventory Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format inFlow Inventory expects, and each action page lists the fields available to sort.

## inFlow Inventory actions that support sorting

- [List Customers](actions/list-customers.md)
- [List Locations](actions/list-locations.md)
- [List Products](actions/list-products.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Stock Adjustments](actions/list-stock-adjustments.md)
- [List Stock Transfers](actions/list-stock-transfers.md)
- [List Vendors](actions/list-vendors.md)
