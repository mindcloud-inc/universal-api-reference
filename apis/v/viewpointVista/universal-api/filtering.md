# Viewpoint Vista Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Viewpoint Vista expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Viewpoint Vista actions that support filtering

- [Search AP Objects](actions/search-ap-objects.md)
- [Search AR Objects](actions/search-ar-objects.md)
- [Search Batch Entries](actions/search-batch-entries.md)
- [Search Batches](actions/search-batches.md)
- [Search DM Objects](actions/search-dm-objects.md)
- [Search EM Objects](actions/search-em-objects.md)
- [Search GL Objects](actions/search-gl-objects.md)
- [Search HQ Objects](actions/search-hq-objects.md)
- [Search IN Objects](actions/search-in-objects.md)
- [Search JC Objects](actions/search-jc-objects.md)
- [Search MS Objects](actions/search-ms-objects.md)
- [Search PM Objects](actions/search-pm-objects.md)
- [Search PO Objects](actions/search-po-objects.md)
- [Search Potential Projects](actions/search-potential-projects.md)
- [Search PR Objects](actions/search-pr-objects.md)
- [Search SL Objects](actions/search-sl-objects.md)
- [Search SM Objects](actions/search-sm-objects.md)
- [Search Transactions](actions/search-transactions.md)
- [Search UD Objects](actions/search-ud-objects.md)
