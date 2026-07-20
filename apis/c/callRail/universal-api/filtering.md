# CallRail Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format CallRail expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## CallRail actions that support filtering

- [List Accounts](actions/list-accounts.md)
- [List Calls](actions/list-calls.md)
- [List Companies](actions/list-companies.md)
- [List Form Submissions](actions/list-form-submissions.md)
- [Summarize Call Data](actions/summarize-call-data.md)
- [Summarize Call Data By Time Series](actions/summarize-call-data-by-time-series.md)
- [Summarize Form Data](actions/summarize-form-data.md)
