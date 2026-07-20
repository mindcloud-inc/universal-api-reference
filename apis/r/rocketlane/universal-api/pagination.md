# Rocketlane Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Rocketlane expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Rocketlane actions that support pagination

- [List Comments](actions/list-comments.md)
- [List Conversations](actions/list-conversations.md)
- [List Invoices](actions/list-invoices.md)
- [List Phases](actions/list-phases.md)
- [List Projects](actions/list-projects.md)
- [List Tasks](actions/list-tasks.md)
- [List Time Entries](actions/list-time-entries.md)
- [List Users](actions/list-users.md)
- [Search Time Entries](actions/search-time-entries.md)
