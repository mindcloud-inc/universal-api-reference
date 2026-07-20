# SAP ERP (S/4HANA) Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format SAP ERP (S/4HANA) expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## SAP ERP (S/4HANA) actions that support filtering

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
