# Katana Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Katana expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Katana actions that support filtering

- [List Current Inventory](actions/list-current-inventory.md)
- [List Customers](actions/list-customers.md)
- [List Inventory Movements](actions/list-inventory-movements.md)
- [List Locations](actions/list-locations.md)
- [List Manufacturing Orders](actions/list-manufacturing-orders.md)
- [List Materials](actions/list-materials.md)
- [List Products](actions/list-products.md)
- [List Purchase Orders](actions/list-purchase-orders.md)
- [List Sales Order Fulfillments](actions/list-sales-order-fulfillments.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Suppliers](actions/list-suppliers.md)
- [List Variants](actions/list-variants.md)
- [List Variants with Negative Stock](actions/list-variants-with-negative-stock.md)
