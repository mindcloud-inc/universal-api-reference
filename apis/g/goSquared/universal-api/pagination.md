# GoSquared Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model GoSquared expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goSquared/latest/actions/get-person-feed?connectionId=$CONNECTION_ID&limit=25&offset=0&personId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## GoSquared actions that support pagination

- [Get Person Feed](actions/get-person-feed.md)
- [List Active Chats](actions/list-active-chats.md)
- [List Archived Chats](actions/list-archived-chats.md)
- [List Devices](actions/list-devices.md)
- [List Smart Group People](actions/list-smart-group-people.md)
- [List Tagged Visitors](actions/list-tagged-visitors.md)
- [Search People](actions/search-people.md)
