# Livestorm Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Livestorm expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-event-people?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Livestorm actions that support pagination

- [List Event People](actions/list-event-people.md)
- [List Event Sessions](actions/list-event-sessions.md)
- [List Events](actions/list-events.md)
- [List People](actions/list-people.md)
- [List People Attributes](actions/list-people-attributes.md)
- [List Session People](actions/list-session-people.md)
- [List Session Questions](actions/list-session-questions.md)
- [List Session Recordings](actions/list-session-recordings.md)
- [List Sessions](actions/list-sessions.md)
- [List Webhooks](actions/list-webhooks.md)
