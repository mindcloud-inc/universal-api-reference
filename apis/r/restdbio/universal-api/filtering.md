# Restdb.io Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Restdb.io expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Restdb.io actions that support filtering

- [Aggregate Documents](actions/aggregate-documents.md)
- [Count Documents](actions/count-documents.md)
- [Group Documents](actions/group-documents.md)
- [List Documents](actions/list-documents.md)
- [List Documents Flattened](actions/list-documents-flattened.md)
- [List Documents With Children](actions/list-documents-with-children.md)
- [List Documents With Linked References](actions/list-documents-with-linked-references.md)
- [List Documents With Media Data](actions/list-documents-with-media-data.md)
- [List Documents With Meta Fields](actions/list-documents-with-meta-fields.md)
- [List Documents With Totals](actions/list-documents-with-totals.md)
- [Search Documents](actions/search-documents.md)
