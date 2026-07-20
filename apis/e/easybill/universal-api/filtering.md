# easybill Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format easybill expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## easybill actions that support filtering

- [List Customers](actions/list-customers.md)
- [List Documents](actions/list-documents.md)
- [List PDF Templates](actions/list-pdf-templates.md)
- [List Position Discounts](actions/list-position-discounts.md)
- [List Position Group Discounts](actions/list-position-group-discounts.md)
- [List Positions](actions/list-positions.md)
- [List Post Boxes](actions/list-post-boxes.md)
- [List Projects](actions/list-projects.md)
- [List Serial Numbers](actions/list-serial-numbers.md)
- [List Stocks](actions/list-stocks.md)
- [List Time Trackings](actions/list-time-trackings.md)
