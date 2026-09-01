# Zenoti Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zenoti expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/get-package-benefits-detail-report?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zenoti actions that support pagination

- [Get Package Benefits Detail Report](actions/get-package-benefits-detail-report.md)
- [Get Sales Accrual Report](actions/get-sales-accrual-report.md)
- [List Appointments By Guest](actions/list-appointments-by-guest.md)
- [Get Appointments Report](actions/list-appointments-flat-file.md)
- [List Center Employee Schedules](actions/list-center-employee-schedules.md)
- [List Center Membership Details](actions/list-center-membership-details.md)
- [List Centers](actions/list-centers.md)
- [Get Collections Report](actions/list-collections.md)
- [List Employees](actions/list-employees.md)
- [List Guest Memberships](actions/list-guest-memberships.md)
- [Get Memberships Report](actions/list-memberships.md)
- [List Purchases By Guest](actions/list-purchases-by-guest.md)
- [Get Sales Report](actions/list-sales.md)
- [List Services](actions/list-services.md)
- [List Therapists](actions/list-therapists.md)
