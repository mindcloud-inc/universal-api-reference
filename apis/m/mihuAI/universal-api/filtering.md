# Mihu AI Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Mihu AI expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Mihu AI actions that support filtering

- [Get All Appointments (Calendar)](actions/get-all-appointments-calendar.md)
- [Get All Schedules](actions/get-all-schedules.md)
- [Get List of Appointment Requests](actions/get-list-of-appointment-requests.md)
- [Get Paginated List of Calls](actions/get-paginated-list-of-calls.md)
- [Get Paginated List of Campaigns](actions/get-paginated-list-of-campaigns.md)
- [Get Paginated List of Contacts](actions/get-paginated-list-of-contacts.md)
- [Get Paginated List of Tasks](actions/get-paginated-list-of-tasks.md)
