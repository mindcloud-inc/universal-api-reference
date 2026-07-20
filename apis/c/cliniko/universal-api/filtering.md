# Cliniko Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format Cliniko expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## Cliniko actions that support filtering

- [List Appointment Types](actions/list-appointment-types.md)
- [List Attendees](actions/list-attendees.md)
- [List Billable Items](actions/list-billable-items.md)
- [List Businesses](actions/list-businesses.md)
- [List Contacts](actions/list-contacts.md)
- [List Group Appointments](actions/list-group-appointments.md)
- [List Individual Appointments](actions/list-individual-appointments.md)
- [List Invoice Items](actions/list-invoice-items.md)
- [List Invoices](actions/list-invoices.md)
- [List Medical Alerts](actions/list-medical-alerts.md)
- [List Patient Cases](actions/list-patient-cases.md)
- [List Patients](actions/list-patients.md)
- [List Practitioners](actions/list-practitioners.md)
- [List Products](actions/list-products.md)
