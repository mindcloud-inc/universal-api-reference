# Eventzilla Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Eventzilla expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventzilla/latest/actions/list-event-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0&eventId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Eventzilla actions that support pagination

- [List Event Transactions](actions/list-event-transactions.md)
- [List Events](actions/list-events.md)
- [List Users](actions/list-users.md)
