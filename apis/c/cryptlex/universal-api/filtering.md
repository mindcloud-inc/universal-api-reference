# Cryptlex Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Cryptlex expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Cryptlex actions that support filtering

- [List Activations](actions/list-activations.md)
- [List Licenses](actions/list-licenses.md)
- [List Products](actions/list-products.md)
- [List Releases](actions/list-releases.md)
- [List Users](actions/list-users.md)
- [List Webhooks](actions/list-webhooks.md)
