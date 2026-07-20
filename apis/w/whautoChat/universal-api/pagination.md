# WhautoChat Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model WhautoChat expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-broadcast-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&broadcastId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## WhautoChat actions that support pagination

- [Get Broadcast Logs](actions/get-broadcast-logs.md)
- [List/Search Broadcasts](actions/list-search-broadcasts.md)
- [List/Search Contact Tags](actions/list-search-contact-tags.md)
- [List/Search Segments](actions/list-search-segments.md)
- [List/Search Staff](actions/list-search-staff.md)
- [List Webhooks](actions/list-webhooks.md)
- [List Workspaces](actions/list-workspaces.md)
- [Search Contacts](actions/search-contacts.md)
