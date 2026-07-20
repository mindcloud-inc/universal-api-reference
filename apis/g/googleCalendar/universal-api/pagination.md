# Google Calendar Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Google Calendar expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCalendar/latest/actions/list-acl-rules?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Google Calendar actions that support pagination

- [List ACL Rules](actions/list-acl-rules.md)
- [List Calendars](actions/list-calendars.md)
- [List Event Instances](actions/list-event-instances.md)
- [List Events](actions/list-events.md)
- [List Settings](actions/list-settings.md)
