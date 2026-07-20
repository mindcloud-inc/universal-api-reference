# MoySklad Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format MoySklad expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## MoySklad actions that support filtering

- [List bundles](actions/list-bundles.md)
- [List counterparties](actions/list-counterparties.md)
- [List countries](actions/list-countries.md)
- [List currencies](actions/list-currencies.md)
- [List customer orders](actions/list-customer-orders.md)
- [List demands](actions/list-demands.md)
- [List employees](actions/list-employees.md)
- [List groups](actions/list-groups.md)
- [List inventories](actions/list-inventories.md)
- [List invoices in](actions/list-invoices-in.md)
- [List invoices out](actions/list-invoices-out.md)
- [List moves](actions/list-moves.md)
- [List organizations](actions/list-organizations.md)
- [List payments in](actions/list-payments-in.md)
- [List payments out](actions/list-payments-out.md)
- [List product folders](actions/list-product-folders.md)
- [List products](actions/list-products.md)
- [List purchase orders](actions/list-purchase-orders.md)
- [List regions](actions/list-regions.md)
- [List services](actions/list-services.md)
- [List stores](actions/list-stores.md)
- [List supplies](actions/list-supplies.md)
- [List variants](actions/list-variants.md)
