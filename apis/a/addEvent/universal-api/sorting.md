# AddEvent Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format AddEvent expects, and each action page lists the fields available to sort.

## AddEvent actions that support sorting

- [Search calendar subscribers](actions/search-calendar-subscribers.md)
- [Search calendars](actions/search-calendars.md)
- [Search events](actions/search-events.md)
- [Search RSVP attendees](actions/search-rsvp-attendees.md)
