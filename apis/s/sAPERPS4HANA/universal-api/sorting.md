# SAP ERP (S/4HANA) Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format SAP ERP (S/4HANA) expects, and each action page lists the fields available to sort.

## SAP ERP (S/4HANA) actions that support sorting

- [List Customer Companies](actions/list-customer-companies.md)
- [List Customer Sales Area Taxes](actions/list-customer-sales-area-taxes.md)
- [List Customer Sales Areas](actions/list-customer-sales-areas.md)
- [List Customer Sales Partner Functions](actions/list-customer-sales-partner-functions.md)
- [List Customers](actions/list-customers.md)
- [List Supplier Companies](actions/list-supplier-companies.md)
- [List Supplier Partner Functions](actions/list-supplier-partner-functions.md)
- [List Supplier Purchasing Organizations](actions/list-supplier-purchasing-organizations.md)
- [List Supplier Withholding Taxes](actions/list-supplier-withholding-taxes.md)
- [List Suppliers](actions/list-suppliers.md)
