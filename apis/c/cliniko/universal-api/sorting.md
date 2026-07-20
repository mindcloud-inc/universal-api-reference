# Cliniko Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Cliniko expects, and each action page lists the fields available to sort.

## Cliniko actions that support sorting

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
