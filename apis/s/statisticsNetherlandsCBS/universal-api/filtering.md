# Statistics Netherlands CBS Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Statistics Netherlands CBS expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Statistics Netherlands CBS actions that support filtering

- [List Category Groups](actions/list-category-groups.md)
- [List Data Properties](actions/list-data-properties.md)
- [List Featured Groups](actions/list-featured-groups.md)
- [List Feed Category Groups](actions/list-feed-category-groups.md)
- [List Feed Data Properties](actions/list-feed-data-properties.md)
- [List Feed Resource Rows](actions/list-feed-resource-rows.md)
- [List Feed Table Infos](actions/list-feed-table-infos.md)
- [List Feed Typed Data Rows](actions/list-feed-typed-data-rows.md)
- [List Feed Untyped Data Rows](actions/list-feed-untyped-data-rows.md)
- [List OData V4 Catalogs](actions/list-o-data-v4-catalogs.md)
- [List OData V4 Datasets](actions/list-o-data-v4-datasets.md)
- [List OData V4 Dimension Codes](actions/list-o-data-v4-dimension-codes.md)
- [List OData V4 Dimension Groups](actions/list-o-data-v4-dimension-groups.md)
- [List OData V4 Dimensions](actions/list-o-data-v4-dimensions.md)
- [List OData V4 Measure Codes](actions/list-o-data-v4-measure-codes.md)
- [List OData V4 Measure Groups](actions/list-o-data-v4-measure-groups.md)
- [List OData V4 Observations](actions/list-o-data-v4-observations.md)
- [List Standard Resource Rows](actions/list-standard-resource-rows.md)
- [List Table Featured Links](actions/list-table-featured-links.md)
- [List Table Infos](actions/list-table-infos.md)
- [List Table Theme Links](actions/list-table-theme-links.md)
- [List Tables](actions/list-tables.md)
- [List Themes](actions/list-themes.md)
- [List Typed Data Rows](actions/list-typed-data-rows.md)
- [List Untyped Data Rows](actions/list-untyped-data-rows.md)
