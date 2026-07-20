# Kladana Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Kladana expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Kladana actions that support filtering

- [List Assortment](actions/list-assortment.md)
- [List Batches](actions/list-batches.md)
- [List Bundles](actions/list-bundles.md)
- [List Contracts](actions/list-contracts.md)
- [List Counterparties](actions/list-counterparties.md)
- [List Countries](actions/list-countries.md)
- [List Currencies](actions/list-currencies.md)
- [List Employees](actions/list-employees.md)
- [List Incoming Payments](actions/list-incoming-payments.md)
- [List Inventory Counts](actions/list-inventory-counts.md)
- [List Organizations](actions/list-organizations.md)
- [List Outgoing Payments](actions/list-outgoing-payments.md)
- [List Product Groups](actions/list-product-groups.md)
- [List Product Variants](actions/list-product-variants.md)
- [List Products](actions/list-products.md)
- [List Projects](actions/list-projects.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Receivings](actions/list-receivings.md)
- [List Sales Invoices](actions/list-sales-invoices.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Services](actions/list-services.md)
- [List Shipments](actions/list-shipments.md)
- [List Supplier Invoices](actions/list-supplier-invoices.md)
- [List Units Of Measure](actions/list-units-of-measure.md)
- [List Warehouses](actions/list-warehouses.md)
