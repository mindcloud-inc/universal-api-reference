# Direct Mail Manager Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Direct Mail Manager expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Direct Mail Manager actions that support filtering

- [List Addresses](actions/list-addresses.md)
- [List Custom Fields](actions/list-custom-fields.md)
- [List Letters](actions/list-letters.md)
- [List Mailing Lists](actions/list-mailing-lists.md)
- [List Postcards](actions/list-postcards.md)
- [List Segments](actions/list-segments.md)
