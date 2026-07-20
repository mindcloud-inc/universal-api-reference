# OnceHub Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model OnceHub expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/list-booking-calendars?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## OnceHub actions that support pagination

- [List Booking Calendars](actions/list-booking-calendars.md)
- [List Booking Pages](actions/list-booking-pages.md)
- [List Bookings](actions/list-bookings.md)
- [List Contacts](actions/list-contacts.md)
- [List Event Types](actions/list-event-types.md)
- [List Master Pages](actions/list-master-pages.md)
- [List Teams](actions/list-teams.md)
- [List Users](actions/list-users.md)
