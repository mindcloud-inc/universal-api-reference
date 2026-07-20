# Typesense Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Typesense expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Typesense actions that support filtering

- [Delete Documents By Query](actions/delete-documents-by-query.md)
- [Get Analytics Events](actions/get-analytics-events.md)
- [Natural Language Search Documents](actions/natural-language-search-documents.md)
- [Search Documents](actions/search-documents.md)
- [Update Documents By Query](actions/update-documents-by-query.md)
- [Vector Search Documents](actions/vector-search-documents.md)
