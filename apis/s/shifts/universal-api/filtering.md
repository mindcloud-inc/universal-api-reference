# 7shifts Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format 7shifts expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## 7shifts actions that support filtering

- [Get User Contacts](actions/get-user-contacts.md)
- [List Companies](actions/list-companies.md)
- [List Departments](actions/list-departments.md)
- [List Employment Records](actions/list-employment-records.md)
- [List Locations](actions/list-locations.md)
- [List Roles](actions/list-roles.md)
- [List Shifts](actions/list-shifts.md)
- [List Time Punches](actions/list-time-punches.md)
- [List Users](actions/list-users.md)
