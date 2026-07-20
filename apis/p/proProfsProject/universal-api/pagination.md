# ProProfs Project Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model ProProfs Project expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## ProProfs Project actions that support pagination

- [List Clients](actions/list-clients.md)
- [List Comments](actions/list-comments.md)
- [List Contacts](actions/list-contacts.md)
- [List Events](actions/list-events.md)
- [List Files](actions/list-files.md)
- [List Projects](actions/list-projects.md)
- [List Tasks](actions/list-tasks.md)
- [List Time Entries](actions/list-time-entries.md)
