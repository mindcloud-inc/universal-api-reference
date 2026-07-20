# Cliniko Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Cliniko expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-appointment-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Cliniko actions that support pagination

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
