# Cerbo Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Cerbo expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-appointment-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Cerbo actions that support pagination

- [List Appointment Types](actions/list-appointment-types.md)
- [List Appointments](actions/list-appointments.md)
- [List Charge Definitions](actions/list-charge-definitions.md)
- [List Encounter Charges](actions/list-encounter-charges.md)
- [List Encounter Estimates](actions/list-encounter-estimates.md)
- [List Encounters](actions/list-encounters.md)
- [List Health Maintenance Trackers](actions/list-health-maintenance-trackers.md)
- [List Inventory](actions/list-inventory.md)
- [List Laboratory Definitions](actions/list-laboratory-definitions.md)
- [List Partner App Orders](actions/list-partner-app-orders.md)
- [List Patient Charges](actions/list-patient-charges.md)
- [List Patient Documents](actions/list-patient-documents.md)
- [List Patient Estimates](actions/list-patient-estimates.md)
- [List Patient Images](actions/list-patient-images.md)
- [List Patient Invoices](actions/list-patient-invoices.md)
- [List Patients](actions/list-patients.md)
- [List Subscriptions](actions/list-subscriptions.md)
- [List Supplements](actions/list-supplements.md)
- [List System-Wide Charges](actions/list-system-wide-charges.md)
- [List Tasks](actions/list-tasks.md)
- [List Users](actions/list-users.md)
- [Search Drugs](actions/search-drugs.md)
- [Search Patients](actions/search-patients.md)
- [Search Supplements](actions/search-supplements.md)
