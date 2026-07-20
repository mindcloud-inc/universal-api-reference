# Level Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Level expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Level actions that support filtering

- [List Alerts](actions/list-alerts.md)
- [List Custom Field Values](actions/list-custom-field-values.md)
- [List Devices](actions/list-devices.md)
- [List Groups](actions/list-groups.md)
- [List Tags](actions/list-tags.md)
