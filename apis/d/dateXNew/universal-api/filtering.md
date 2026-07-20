# DateX Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format DateX expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## DateX actions that support filtering

- [List Available Inventory](actions/list-available-inventory.md)
- [List Carriers](actions/list-carriers.md)
- [List Inventory](actions/list-inventory.md)
- [List Materials](actions/list-materials.md)
- [List Owners](actions/list-owners.md)
- [List Sales Orders](actions/list-sales-orders.md)
- [List Sales Shipments](actions/list-sales-shipments.md)
- [List Shipping Details](actions/list-shipping-details.md)
- [List Warehouses](actions/list-warehouses.md)
