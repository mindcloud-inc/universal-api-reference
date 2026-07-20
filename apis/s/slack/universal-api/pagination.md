# Slack Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Slack expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/get-file-information?connectionId=$CONNECTION_ID&limit=25&offset=0&channel=string&file=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Slack actions that support pagination

- [Get File Information](actions/get-file-information.md)
- [List Channel Messages](actions/list-channel-messages.md)
- [List Channels](actions/list-channels.md)
- [List Files](actions/list-files.md)
- [List Scheduled Messages](actions/list-scheduled-messages.md)
- [List Users](actions/list-users.md)
- [Search Channels and Users](actions/search-channels-and-users.md)
