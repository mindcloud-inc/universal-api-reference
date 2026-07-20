# TicketSource Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model TicketSource expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketSource/latest/actions/list-booking-seats?connectionId=$CONNECTION_ID&limit=25&offset=0&bookingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## TicketSource actions that support pagination

- [List Booking Seats](actions/list-booking-seats.md)
- [List Customer Bookings](actions/list-customer-bookings.md)
- [List Customer Notes](actions/list-customer-notes.md)
- [List Customers](actions/list-customers.md)
- [List Date Bookings](actions/list-date-bookings.md)
- [List Event Dates](actions/list-event-dates.md)
- [List Event Venues](actions/list-event-venues.md)
- [List Events](actions/list-events.md)
- [List Venue Dates](actions/list-venue-dates.md)
