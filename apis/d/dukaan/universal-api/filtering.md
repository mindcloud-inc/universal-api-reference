# Dukaan Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Dukaan expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Dukaan actions that support filtering

- [List Discounts](actions/list-discounts.md)
- [List Orders](actions/list-orders.md)
- [List Products By Category](actions/list-products-by-category.md)
- [List Warehouses](actions/list-warehouses.md)
- [Search Orders](actions/search-orders.md)
- [Search Product Categories](actions/search-product-categories.md)
- [Search Products](actions/search-products.md)
