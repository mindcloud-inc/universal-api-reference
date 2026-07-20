# Hub Planner Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Hub Planner expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/list-billing-rates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Hub Planner actions that support pagination

- [List Billing Rates](actions/list-billing-rates.md)
- [List Booking Categories](actions/list-booking-categories.md)
- [List Bookings](actions/list-bookings.md)
- [List Clients](actions/list-clients.md)
- [List Events](actions/list-events.md)
- [List Holidays](actions/list-holidays.md)
- [List Project Groups](actions/list-project-groups.md)
- [List Projects](actions/list-projects.md)
- [List Resource Groups](actions/list-resource-groups.md)
- [List Resources](actions/list-resources.md)
- [List Time Entries](actions/list-time-entries.md)
- [Search Billing Rates](actions/search-billing-rates.md)
- [Search Booking Categories](actions/search-booking-categories.md)
- [Search Bookings](actions/search-bookings.md)
- [Search Clients](actions/search-clients.md)
- [Search Events](actions/search-events.md)
- [Search Holidays](actions/search-holidays.md)
- [Search Projects](actions/search-projects.md)
- [Search Resources](actions/search-resources.md)
- [Search Time Entries](actions/search-time-entries.md)
