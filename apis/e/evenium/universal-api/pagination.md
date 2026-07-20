# Evenium Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Evenium expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-event-part-registrations?connectionId=$CONNECTION_ID&limit=25&offset=0&eventId=1&eventPartId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Evenium actions that support pagination

- [List Event Part Registrations](actions/list-event-part-registrations.md)
- [List Event Parts](actions/list-event-parts.md)
- [List Events](actions/list-events.md)
- [List Guests](actions/list-guests.md)
