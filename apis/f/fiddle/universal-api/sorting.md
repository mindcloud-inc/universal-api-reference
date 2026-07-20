# Fiddle Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Fiddle expects, and each action page lists the fields available to sort.

## Fiddle actions that support sorting

- [List Customers](actions/list-customers.md)
- [List Inventory Items](actions/list-inventory-items.md)
- [List Inventory Locations](actions/list-inventory-locations.md)
- [List Inventory Lots](actions/list-inventory-lots.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Quarantined Lots](actions/list-quarantined-lots.md)
- [List Sales Order Items](actions/list-sales-order-items.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Suppliers](actions/list-suppliers.md)
- [List Work Orders](actions/list-work-orders.md)
