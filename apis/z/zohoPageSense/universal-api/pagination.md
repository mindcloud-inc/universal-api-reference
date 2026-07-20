# Zoho PageSense Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Zoho PageSense expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/day-wise-stats-reports?connectionId=$CONNECTION_ID&limit=25&offset=0&portalName=Ava%20Chen&fullTrackingReports.startDate=2026-05-07T12%3A00%3A00.000Z&fullTrackingReports.endDate=2026-05-07T12%3A00%3A00.000Z&fullTrackingReports.primaryDimension=string&fullTrackingReports.metrics=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Zoho PageSense actions that support pagination

- [Day-Wise Stats Reports](actions/day-wise-stats-reports.md)
- [Individual Stats Report](actions/individual-stats-report.md)
- [Total Stats Report](actions/total-stats-report.md)
