# AddEvent Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model AddEvent expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/search-calendar-subscribers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## AddEvent actions that support pagination

- [Search calendar subscribers](actions/search-calendar-subscribers.md)
- [Search calendars](actions/search-calendars.md)
- [Search events](actions/search-events.md)
- [Search RSVP attendees](actions/search-rsvp-attendees.md)
