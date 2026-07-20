# Persona Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Persona expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Persona actions that support filtering

- [List Accounts](actions/list-accounts.md)
- [List API keys](actions/list-api-keys.md)
- [List Cases](actions/list-cases.md)
- [List Connections](actions/list-connections.md)
- [List Devices](actions/list-devices.md)
- [List Events](actions/list-events.md)
- [List Inquiries](actions/list-inquiries.md)
- [List Inquiry Sessions](actions/list-inquiry-sessions.md)
- [List Lists](actions/list-lists.md)
- [List Reports](actions/list-reports.md)
- [List Share Tokens](actions/list-share-tokens.md)
- [List Transactions](actions/list-transactions.md)
- [List Workflow Runs](actions/list-workflow-runs.md)
