# Priority Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Priority expects, and each action page lists the fields available to sort.

## Priority actions that support sorting

- [List AP Invoices](actions/list-ap-invoices.md)
- [List AR Invoices](actions/list-ar-invoices.md)
- [List Banks](actions/list-banks.md)
- [List Companies](actions/list-companies.md)
- [List Countries](actions/list-countries.md)
- [List Currencies](actions/list-currencies.md)
- [List Customer Documents](actions/list-customer-documents.md)
- [List Customers](actions/list-customers.md)
- [List Document Types](actions/list-document-types.md)
- [List Part Balances](actions/list-part-balances.md)
- [List Parts](actions/list-parts.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Quotation Documents](actions/list-quotation-documents.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Shippers](actions/list-shippers.md)
- [List Suppliers](actions/list-suppliers.md)
- [List Users](actions/list-users.md)
- [List Warehouses](actions/list-warehouses.md)
