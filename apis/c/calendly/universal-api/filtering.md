# Calendly Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Calendly expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Calendly actions that support filtering

- [List Event Invitees](actions/list-event-invitees.md)
- [List Event Type Available Times](actions/list-event-type-available-times.md)
- [List Routing Form Submissions](actions/list-routing-form-submissions.md)
- [List Scheduled Events](actions/list-scheduled-events.md)
- [List User Busy Times](actions/list-user-busy-times.md)
