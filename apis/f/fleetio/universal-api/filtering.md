# Fleetio Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Fleetio expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Fleetio actions that support filtering

- [List Contacts](actions/list-contacts.md)
- [List Fuel Entries](actions/list-fuel-entries.md)
- [List Issues](actions/list-issues.md)
- [List Meter Entries](actions/list-meter-entries.md)
- [List Service Entries](actions/list-service-entries.md)
- [List Vehicles](actions/list-vehicles.md)
- [List Vendors](actions/list-vendors.md)
- [List Work Orders](actions/list-work-orders.md)
