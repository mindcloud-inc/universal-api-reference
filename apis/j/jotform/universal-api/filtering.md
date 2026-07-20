# Jotform Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Jotform expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Jotform actions that support filtering

- [List Form Submissions](actions/list-form-submissions.md)
- [List Sub-User Accounts](actions/list-sub-user-accounts.md)
- [List User Forms](actions/list-user-forms.md)
- [List User History](actions/list-user-history.md)
- [List User Invoices](actions/list-user-invoices.md)
- [List User Reports](actions/list-user-reports.md)
- [List User Submissions](actions/list-user-submissions.md)
